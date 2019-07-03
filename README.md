# my-note
## 原型链的理解
### 构造函数与原型
- 构造函数时会自动创建一个原型prototype
- 创建新实例时，实例中的prototype指向该构造函数的原型对象
- 原型中含有constructor指向构造函数
### 原型链
‘function SuperType() {
        this.property = true;
    }
    SuperType.prototype.getSuperValue = function() {
        return this.property;
    };
    function SubType() {
        this.subproperty = false;
    }
    SubType.prototype = new SuperType();
    SubType.prototype.getSubValue = function() {
        return this.subproperty;
    };
    var instance = new SubType();
    alert(instance.getSuperValue());’

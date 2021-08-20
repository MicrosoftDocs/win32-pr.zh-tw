---
title: 略過屬性
description: '\ 忽略 \ 屬性會指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。 \ 忽略 \ 屬性僅限於結構或等位的指標成員。'
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- 忽略屬性 MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6b7a1e70804bc3c9c277f3d46ac6a8ad20fc0f98b370f93fe9fd09b0b1bb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013856"
---
# <a name="ignore-attribute"></a>略過屬性

**\[ Ignore \]** 屬性會指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。 **\[ Ignore \]** 屬性僅限於結構或等位的指標成員。

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*指標成員類型* 
</dt> <dd>

指定結構或等位之指標成員的類型。

</dd> <dt>

*指標名稱* 
</dt> <dd>

指定在封送處理期間要忽略之指標成員的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

目的地端未定義具有 **\[ ignore \]** 屬性之結構成員的值。 **\[**[**在**](in.md) **\]** 遠端電腦上未定義 in 參數。 **\[** [](out-idl.md) **\]** 在本機電腦上未定義 out 參數。

**\[ Ignore \]** 屬性可讓您防止資料的傳輸。 這在類似于雙重連結清單的情況下很有用。 下列範例包含會導入資料別名的雙重連結清單：

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

在上述範例中會發生別名，因為在函式 **p** 和 **p >下一個 >** 的兩個不同指標中，可以使用相同的記憶體區域。

請注意，[ **\[ 忽略 \]** ] 不能用來做為類型屬性。

## <a name="examples"></a>範例

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 
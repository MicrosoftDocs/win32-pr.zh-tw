---
title: void 屬性
description: 基底類型 void 表示沒有引數的程式，或未傳回結果值的程式。
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void 屬性 MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106994953"
---
# <a name="void-attribute"></a>void 屬性

基底類型 **void** 表示沒有引數的程式，或未傳回結果值的程式。

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*parameter-list* 
</dt> <dd>

指定傳遞至函式的參數清單，以及相關聯的參數類型和參數屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

指定函數所傳回之類型的名稱。

</dd> <dt>

*內容-控制碼類型* 
</dt> <dd>

指定採用 **\[** [**內容 \_ 控制碼**](context-handle.md)屬性之類型的名稱 **\]** 。

</dd> </dl>

## <a name="remarks"></a>備註

指標類型 **\* void**（以 C 描述可轉換成代表任何指標類型的泛型指標）在 MIDL 中會限制為與 **\[ 內容 \_ 控制碼 \]** 關鍵字搭配使用。

## <a name="examples"></a>範例

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> </dl>

 

 





---
description: 將範本儲存至 DirectX 檔案。 已取代。
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'IDirectXFileSaveObject：： SaveTemplates 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 87ec95932b26877354c22089a97b249bd542aa841552c3e3f9e4827a20f6d608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292219"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>IDirectXFileSaveObject：： SaveTemplates 方法

將範本儲存至 DirectX 檔案。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cTemplates* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要儲存的範本總數。

</dd> <dt>

*ppguidTemplates* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \* \***

要儲存之所有範本的 Guid 陣列指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。

## <a name="remarks"></a>備註

下列程式碼片段提供 **IDirectXFileSaveObject：： SaveTemplates** 的範例呼叫，以及 ppguidTemplates 點的陣列範例內容。


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



使用這個方法來儲存範本之後，請使用 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立資料物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 

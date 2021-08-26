---
description: 註冊自訂範本。 已取代。
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'IDirectXFile：： RegisterTemplates 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 685e97ec28241348ff4a969c444b6da5638aeba01af8be35cc5490a0d2be0a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846958"
---
# <a name="idirectxfileregistertemplates-method"></a>IDirectXFile：： RegisterTemplates 方法

註冊自訂範本。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pvData* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

緩衝區的指標，此緩衝區是由包含範本的文字或二進位格式的 DirectX 檔案所組成。

</dd> <dt>

*cbSize* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

PvData 所指向的緩衝區大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADFILEFLOATSIZE、DXFILEERR \_ BADFILETYPE、DXFILEERR \_ BADFILEVERSION、DXFILEERR \_ BADVALUE、DXFILEERR \_ PARSEERROR。

## <a name="remarks"></a>備註

下列程式碼片段提供 **RegisterTemplates** 的範例呼叫，以及 pvData 所指向之緩衝區的範例內容。


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



所有範本都必須指定名稱，以及 (UUID) 的通用唯一識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 

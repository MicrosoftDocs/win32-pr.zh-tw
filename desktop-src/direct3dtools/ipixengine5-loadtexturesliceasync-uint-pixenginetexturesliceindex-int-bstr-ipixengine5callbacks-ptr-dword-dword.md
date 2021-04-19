---
description: 載入紋理配量，並在完成時通知主機 asynchrnously。
MS-HAID: vspixengine.IPixEngine5\_LoadTextureSliceAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： LoadTextureSliceAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 520DBB6D-D8F3-451F-942C-BE8428B9ADFF
api_name:
- IPixEngine5.LoadTextureSliceAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 505ccfd6668cbe08b4f62878b5f51e9c20185b41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972310"
---
# <a name="span-idvspixengineipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturesliceasync-method"></a><span id="vspixengine.ipixengine5_loadtexturesliceasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： LoadTextureSliceAsync 方法

載入紋理配量，並在完成時通知主機 asynchrnously。

## <a name="syntax"></a>語法


```C++
HRESULT LoadTextureSliceAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*textureId*   
要載入配量的材質識別碼。

*sliceIndex*   
要載入之配量的索引。

*formatOverride*   
指定格式覆寫。

*histogramDataFileName*   
COM 字串，其中包含與材質配量相關聯的長條圖資料檔案名稱。

*回檔*   
提供 IPixEngine5 回呼介面之物件的位址。

*requestCookie*   
可唯一識別要求的 cookie，而且可用來指示它被取消。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 

---
description: WriteBitmapBits 方法會在指定的媒體時間取出影片畫面，並將其寫入檔案。 影片框架一律採用24位 RGB 格式。
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'IMediaDet：： WriteBitmapBits 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc2a967f5b0e99c50317e9dc226a4b345c6790a8ce2b6e5d42eb50dfdc3b105b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154153"
---
# <a name="imediadetwritebitmapbits-method"></a>IMediaDet：： WriteBitmapBits 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`WriteBitmapBits`方法會在指定的媒體時間取出影片畫面，並將其寫入檔案。 影片框架一律採用24位 RGB 格式。

## <a name="syntax"></a>語法


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StreamTime* 
</dt> <dd>

取出影片畫面的時間。

</dd> <dt>

*寬度* 
</dt> <dd>

影像的寬度（以圖元為單位）。

</dd> <dt>

*高度* 
</dt> <dd>

影像的高度（以圖元為單位）。

</dd> <dt>

*檔案名稱* 
</dt> <dd>

要在其中儲存點陣圖之檔案的路徑。 如果檔案已存在，這個方法會覆寫該檔案。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 \_ ，確定成功。 否則，會傳回 **HRESULT** 值，指出錯誤的原因。 可能的錯誤代碼包括下列各項：



| 傳回碼                                                                                             | 描述                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | 無法將 [**範例捕獲**](sample-grabber-filter.md) 篩選新增至圖形。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                  | 失敗。<br/>                                                                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | 記憶體不足。<br/>                                                                   |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>            | 非預期的錯誤。<br/>                                                                      |
| <dl> <dt>**STG. \_ E \_ ACCESSDENIED**</dt> </dl>     | 無法覆寫檔案。<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 媒體類型無效。<br/>                                                                    |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)

這個方法會將媒體偵測器放入點陣圖抓取模式。 一旦呼叫這個方法，除非您建立新的媒體偵測器實例，否則 **IMediaDet** 中的各種資料流程資訊方法將無法運作。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaDet 介面**](imediadet.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: GetBitmapBits 方法會在指定的媒體時間取出影片畫面。 傳回的框架一律採用24位 RGB 格式。
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'IMediaDet：： GetBitmapBits 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000436"
---
# <a name="imediadetgetbitmapbits-method"></a>IMediaDet：： GetBitmapBits 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetBitmapBits`方法會在指定的媒體時間取出影片畫面。 傳回的框架一律採用24位 RGB 格式。

## <a name="syntax"></a>語法


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StreamTime* 
</dt> <dd>

取出影片畫面的時間（以秒為單位）。

</dd> <dt>

*pBufferSize* 
</dt> <dd>

接收所需的緩衝區大小。 如果 *pBuffer* 為 **Null**，則變數會收到取出框架所需的緩衝區大小。 如果 *pBuffer* 不是 **Null**，則會忽略此參數。

</dd> <dt>

*pBuffer* 
</dt> <dd>

緩衝區的指標，此緩衝區會接收 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構，後面接著 DIB 位。

</dd> <dt>

*寬度* 
</dt> <dd>

影片影像的寬度（以圖元為單位）。

</dd> <dt>

*高度* 
</dt> <dd>

影片影像的高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                                             | Description                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | 無法將 [**範例捕獲**](sample-grabber-filter.md) 篩選新增至圖形。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | 記憶體不足。<br/>                                                                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標錯誤。<br/>                                                                |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>            | 非預期的錯誤。<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 媒體類型無效。<br/>                                                                    |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)

若要判斷所需的緩衝區大小，請使用等於 **Null** 的 *pBuffer* 呼叫這個方法。 大小會在 *pBufferSize* 所指向的變數中傳回。 然後建立緩衝區，並再次呼叫方法，其 *pBuffer* 等於緩衝區的位址。 當方法傳回時，緩衝區會包含 **BITMAPINFOHEADER** 結構，後面接著點陣圖。 點陣圖會調整為 [ *寬度* ] 和 [ *高度* ] 參數中所指定的維度。

這個方法會將媒體偵測器放入點陣圖抓取模式。 一旦呼叫這個方法，除非您建立新的媒體偵測器實例，否則 **IMediaDet** 中的各種資料流程資訊方法將無法運作。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="examples"></a>範例

下列程式碼會使用 `GetBitmapBits` 方法來建立與裝置無關的點陣圖。


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



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

 

 





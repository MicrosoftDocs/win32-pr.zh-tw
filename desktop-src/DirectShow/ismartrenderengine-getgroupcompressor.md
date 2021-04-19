---
description: GetGroupCompressor 方法會抓取指定群組的壓縮篩選。
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'ISmartRenderEngine：： GetGroupCompressor 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978729"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>ISmartRenderEngine：： GetGroupCompressor 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetGroupCompressor` 指定群組的壓縮篩選。

## <a name="syntax"></a>語法


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*群組* 
</dt> <dd>

群組以零為基底的索引。

</dd> <dt>

*pCompressor* 
</dt> <dd>

接收壓縮篩選之 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。 如果沒有壓縮篩選，則會接收 **Null** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用這個方法可設定壓縮篩選的屬性，例如，主要畫面格速率。 請在呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md)之後，但在轉譯專案之前呼叫這個方法。 然後查詢壓縮篩選器的輸出圖釘以取得 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面，其中包含設定壓縮參數的方法。 當您完成時，請釋放介面。 如果您對時間軸進行任何後續的變更，請呼叫 **ConnectFrontEnd**，然後再次呼叫 **GetGroupCompressor** ，以重設壓縮參數。

傳回時，如果 pCompressor 的值 \* 為非 **Null**，則 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISmartRenderEngine 介面**](ismartrenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 





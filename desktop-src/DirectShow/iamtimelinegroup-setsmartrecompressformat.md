---
description: SetSmartRecompressFormat 方法會指定要用於智慧型 recompression 的影片壓縮格式。
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'IAMTimelineGroup：： SetSmartRecompressFormat 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995959"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>IAMTimelineGroup：： SetSmartRecompressFormat 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetSmartRecompressFormat`方法會指定要用於智慧型 recompression 的影片壓縮格式。

音訊群組不支援 Smart recompression。

## <a name="syntax"></a>語法


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pformatetc 架構* 
</dt> <dd>

描述壓縮格式之結構的指標。 目前，只有 [**SCompFmt0**](scompfmt0.md) 結構有效。 您必須將此參數轉換為 **long** 類型的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

在呼叫這個方法之前，請在相同群組上呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法，以指定未壓縮的格式。

如果 `SetSmartRecompressFormat` 方法成功，您可以使用智慧型轉譯引擎來輸出壓縮的影片資料流程。 壓縮的影片將會有在 *pformatetc 架構* 參數中指定的寬度、高度和畫面播放速率。 這些值將會覆寫 **SetMediaType** 方法中針對未壓縮格式所指定的值。 不過，若要取得智慧 recompression 的優點，這兩種格式應該相符。 換句話說，壓縮和未壓縮的格式應該具有相同的高度、寬度和畫面播放速率。

如果智慧型轉譯引擎無法產生壓縮的格式，則會改為產生未壓縮的影片資料流程。 如果發生這種情況，智慧轉譯引擎會報告 DEX \_ 識別碼在 \_ \_ \_ [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法期間找不到壓縮程式轉譯錯誤。 應用程式可以透過 [**IAMErrorLog：： LogError**](iamerrorlog-logerror.md) 方法攔截這個錯誤。  (如需詳細資訊，請參閱 [記錄錯誤](logging-errors.md) 和轉譯 [錯誤](rendering-errors.md)。 ) 

智慧型 recompression 格式不是持續性。 如果應用程式使用智慧型 recompression，它必須在每次載入專案檔時設定 recompression 格式。

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

[**IAMTimelineGroup 介面**](iamtimelinegroup.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[智慧型轉譯引擎](smart-render-engine.md)
</dt> <dt>

[將專案寫入檔案](writing-a-project-to-a-file.md)
</dt> </dl>

 

 





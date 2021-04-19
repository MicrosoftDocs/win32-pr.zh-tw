---
title: _WAVEFORMATEX 結構
description: '\_WAVEFORMATEX 結構會定義波形音訊資料的格式。'
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989752"
---
# <a name="_waveformatex-structure"></a>\_WAVEFORMATEX 結構

**\_ WAVEFORMATEX** 結構會定義波形音訊資料的格式。

## <a name="syntax"></a>語法


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>成員

<dl> <dt>

**wFormatTag**
</dt> <dd>

必須設定為裝置支援的格式或格式。 請注意，舊版 Windows Media 裝置管理員建議您使用 WMDM \_ WAVE \_ FORMAT \_ all 來指出所有格式的支援。 不過，這不再是建議的作法，因為不同的媒體播放機會以不同的方式來解讀這一點，而只有少數裝置才能真正播放任何檔案格式。 現在建議您使用 WMDM \_ 列舉 \_ \_ \_ 的有效值 \_ ，以提供任何 [**WMDM 列舉的有效值 \_ \_ \_ \_ \_ 形式**](wmdm-enum-prop-valid-values-form.md) 列舉值，或更好的方式，同時使用 [**WMDM 的 \_ \_ 值 \_ 範圍**](wmdm-prop-values-range.md) 結構來指定格式範圍。

</dd> <dt>

**nChannels**
</dt> <dd>

波形音訊資料中的通道數目。 Monaural 資料會使用一個通道，而身歷聲資料會使用兩個通道。

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

取樣率，以每秒樣本數 (赫茲) ，每個通道都必須播放或記錄。 **NSamplesPerSec** 的常見值是8.0 千赫茲 (kHz) 、11.025 kHz、22.05 khz 和 44.1 khz。

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

格式標記需要的平均資料傳輸速率（以每秒位元組數為單位）。 播放和錄製軟體可以使用 **nAvgBytesPerSec** 成員來預估緩衝區大小。

</dd> <dt>

**nBlockAlign**
</dt> <dd>

區塊對齊（以位元組為單位）。 區塊對齊是 **wFormatTag** 格式類型資料的最小不可部分完成單位。 播放和錄製軟體必須一次處理 **nBlockAlign** 個位元組的資料。 從裝置寫入和讀取的資料必須一律從區塊的開頭開始。 例如，無法在範例 (（也就是在不封鎖對齊) 的界限）上，正確地開始播放 PCM 資料。

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

**WFormatTag** 格式類型的每個樣本位數。

</dd> <dt>

**cbSize**
</dt> <dd>

忽略這個成員。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 






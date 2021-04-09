---
description: 完成元資料緩衝區所需的任何作業，並釋放指定的 ISpatialAudioMetadataItems 物件。
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: ISpatialAudioMetadataWriter：： Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111196"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>ISpatialAudioMetadataWriter：： Close 方法

完成元資料緩衝區所需的任何作業，並釋放指定的 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT Close();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，可能的傳回碼包括（但不限於）下表所示的值。



| 傳回碼                                                                                                                     | Description                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CONTOSO-CLNT \_ E \_ 未 \_ 開啟任何專案 \_**</dt> </dl>            | 未開啟具有 [**開啟**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open)之呼叫的已提供 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) 。<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CONTOSO-CLNT \_ E \_ 未 \_ 寫入任何專案 \_**</dt> </dl>         | 未將任何中繼資料專案寫入提供的 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)。<br/>                                              |
| <dl> <dt>**SPTLAUD \_ MD \_ CONTOSO-CLNT \_ E \_ 專案 \_ 必須 \_ 有 \_ 命令**</dt> </dl> | 未將任何中繼資料命令寫入提供的 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)。<br/>                                           |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 





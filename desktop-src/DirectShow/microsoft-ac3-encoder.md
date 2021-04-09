---
description: Microsoft AC-3 編碼器篩選器會將身歷聲 PCM 音訊編碼為杜比數位位流。
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: 'Microsoft AC-3 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109180"
---
# <a name="microsoft-ac-3-encoder"></a>Microsoft AC-3 編碼器

Microsoft AC-3 編碼器篩選器會將身歷聲 PCM 音訊編碼為杜比數位位流。

> [!Note]  
> Microsoft 應用程式使用的杜比數位授權方案，會限制 Microsoft 的杜比數位技術。

 

> [!Note]  
> 以 IA-64 為基礎的平臺不支援此篩選器。

 



篩選資訊

篩選介面

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

輸入 Pin 媒體類型

**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ PCM**<br/> 輸入類型必須是 48-kHz 身歷聲，每個樣本16位。<br/>

輸入 Pin 介面

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

輸出 Pin 媒體類型

**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ AC3**<br/> **媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ 杜比 \_ AC3**<br/>

輸出 Pin 介面

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

篩選 CLSID

**CLSID \_** 在 wmcodecdsp 中宣告的 CMSAC3Enc () 

可執行檔

msac3enc.dll

[優點](merit.md)

**\_ \_ 未 \_ 使用的業績**

[篩選準則分類](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>備註

此篩選器無法供協力廠商應用程式使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>                                                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 





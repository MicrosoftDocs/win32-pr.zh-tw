---
description: Windows Media MPEG-2 V3 解碼會解碼 MPEG-2 V3 影片串流。
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: 'Windows Media MPEG-2 V3 解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106988097"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Media MPEG-2 V3 解碼器

Windows Media MPEG-2 V3 解碼會解碼 MPEG-2 V3 影片串流。

## <a name="class-identifier"></a>類別識別碼

Windows MPEG-2 V3 解碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMpeg43DecMediaObject** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立 mpeg-2 V3 解碼器的實例。

## <a name="formats"></a>格式

Windows Media MPEG-2 V3 解碼支援下列輸入媒體類型。

-   MEDIASUBTYPE \_ MP43
-   MEDIASUBTYPE \_ mp43

當 Windows Media MPEG-2 V3 解碼器作為 DirectX 媒體物件 (的) 時，支援下列輸出媒體子類型。

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

當 Windows Media MPEG-2 V3 解碼器作為媒體基礎轉換 (MFT) 時，支援下列輸出媒體子類型。

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>備註

Windows Media MPEG-2 V3 解碼物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。 物件具有相同的類別識別碼 (CLSID) ，不論它是以 SQL-DMO 或 MFT 的形式。

根據您取得的介面以及正在執行的 Windows 版本而定，MPEG 4 V3 解碼器會以一或 MFT 的形式運作。 下表顯示的是 MPEG-2 V3 解碼器以 SQL-DMO 或 MFT 行為的條件。



| 作業系統            | 解碼器行為                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | MPEG-2 V3 解碼器的行為一律會是 SQL-DMO。                                                                                                                      |
| Windows Vista 和 Windows 7 | 根據預設，MPEG 4 V3 解碼器的行為就像是一。 如果您在 MPEG 4 V3 解碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。 |



 

針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據解碼器是以 SQL-DMO 或 MFT 作為依據而有所不同。 非 RGB 媒體子類型的 Guid 是相同的，不論是以 SQL-DMO 或 MFT 的形式來表示。 如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 

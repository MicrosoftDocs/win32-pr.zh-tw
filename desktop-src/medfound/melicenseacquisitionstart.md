---
description: 當授權取得即將開始時，由原則引擎引發。 授權取得是使用 IMFContentProtectionManager 介面的應用程式實作為執行。
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: 'MELicenseAcquisitionStart 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989301"
---
# <a name="melicenseacquisitionstart-event"></a>MELicenseAcquisitionStart 事件

當授權取得即將開始時，由原則引擎引發。 授權取得是使用應用程式的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面實作為執行。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

當授權取得完成時，原則引擎會引發 [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 





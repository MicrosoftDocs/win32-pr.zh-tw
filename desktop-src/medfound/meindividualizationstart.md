---
description: 當您要開始使用時，由原則引擎引發。 您可以使用 IMFContentProtectionManager 介面的應用程式執行來執行個人化。
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: 'MEIndividualizationStart 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997108"
---
# <a name="meindividualizationstart-event"></a>MEIndividualizationStart 事件

當您要開始使用時，由原則引擎引發。 您可以使用應用程式的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面執行來執行個人化。

個別的應用程式是指其數位版權管理的升級 (DRM) 元件，其與相同應用程式的所有其他複本有所區別。 內容擁有者可以要求只能在已個人化的應用程式上播放其受保護的檔案。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

當授權取得完成時，原則引擎會引發 [MEIndividualizationCompleted](meindividualizationcompleted.md) 事件。

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

 

 





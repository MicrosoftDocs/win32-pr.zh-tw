---
description: 當您要開始使用時，由原則引擎引發。 您可以使用 IMFContentProtectionManager 介面的應用程式執行來執行個人化。
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: 'MEIndividualizationStart 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297ed3dea2dbdfe45a8ea812b7a5c674e1ef1bfb1c136aa54cfd5cd463cf9b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957448"
---
# <a name="meindividualizationstart-event"></a>MEIndividualizationStart 事件

當您要開始使用時，由原則引擎引發。 您可以使用應用程式的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面執行來執行個人化。

個別的應用程式是指其數位版權管理的升級 (DRM) 元件，其與相同應用程式的所有其他複本有所區別。 內容擁有者可以要求只能在已個人化的應用程式上播放其受保護的檔案。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

當授權取得完成時，原則引擎會引發 [MEIndividualizationCompleted](meindividualizationcompleted.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 





---
description: 進行串流時發生非嚴重錯誤。
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: 'MENonFatalError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318824"
---
# <a name="menonfatalerror-event"></a>MENonFatalError 事件

進行串流時發生非嚴重錯誤。 任何媒體基礎元件都可以隨時傳送此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE            | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| VT \_ UI4<br/> | 描述錯誤的 **HRESULT** 值。<br/> <br/> |



## <a name="attributes"></a>屬性

未定義此事件的屬性。

## <a name="remarks"></a>備註

此事件會在串流處理期間發出未預期但可復原的錯誤。 例如，如果媒體來源卸載封包，則可能會傳送此事件。

請勿傳送此事件來表示非同步方法失敗。 如果非同步方法失敗，則會在該方法的正常事件中傳回錯誤碼。

如果發生無法復原的串流錯誤，請傳送 [MEError](meerror.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 





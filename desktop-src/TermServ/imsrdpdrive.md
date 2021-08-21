---
title: IMsRdpDrive 介面
description: 包含磁片磁碟機物件的相關資訊。
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- IMsRdpDrive 介面遠端桌面服務
- IMsRdpDrive 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efccf0459375e23375b3ac40067bcbd3965ed7f6c0b51ddb60f6362fb419688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000728"
---
# <a name="imsrdpdrive-interface"></a>IMsRdpDrive 介面

包含磁片磁碟機物件的相關資訊。

## <a name="members"></a>成員

**IMsRdpDrive** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpDrive** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpDrive** 介面具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**名稱**](imsrdpdrive-name.md)<br/>                         | 唯讀<br/>  | 抓取磁片磁碟機的名稱。<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | 讀取/寫入<br/> | 指出磁片磁碟機的重新導向狀態。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive 定義為 d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 


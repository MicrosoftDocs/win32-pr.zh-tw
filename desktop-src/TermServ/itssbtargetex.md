---
title: ITsSbTargetEx 介面
description: 公開屬性，這些屬性會儲存目標的設定和狀態資訊。
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- ITsSbTargetEx 介面遠端桌面服務
- ITsSbTargetEx 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fb9be0e4cf5c0395efa93d308fdfa45362a7ac8919ab49a108700106aff6081b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989818"
---
# <a name="itssbtargetex-interface"></a>ITsSbTargetEx 介面

公開屬性，這些屬性會儲存目標的設定和狀態資訊。

只有在已安裝[KB3091411](https://support.microsoft.com/kb/3091411)的 Windows Server 2012 R2 上才能使用此介面。 從 Windows Server 2016 開始，可以使用 [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)介面的 [**TargetLoad**](itssbtarget-targetload.md)屬性。

## <a name="members"></a>成員

**ITsSbTargetEx** 介面繼承自 [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)。 **ITsSbTargetEx** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ITsSbTargetEx** 介面具有這些屬性。



| 屬性                                                                      | 存取類型           | 描述                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | 讀取/寫入<br/> | 抓取或指定與目標相關聯之環境的名稱。<br/> |
| [**FarmName**](itssbtarget-farmname.md)<br/>                           | 讀取/寫入<br/> | 指定或抓取這個目標所聯結的伺服器陣列名稱。<br/>    |
| [**IpAddresses**](itssbtarget-ipaddresses.md)<br/>                     | 讀取/寫入<br/> | 捕獲或指定目標的外部 IP 位址。<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | 唯讀<br/>  | 抓取目標的暫止使用者連接數目。<br/>               |
| [**NumSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | 唯讀<br/>  | 抓取 broker 針對目標所維護的會話數目。<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | 讀取/寫入<br/> | 指定或抓取目標的完整功能變數名稱。<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | 唯讀<br/>  | 抓取目標的相對負載。<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | 讀取/寫入<br/> | 指定或抓取目標的名稱。<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | 讀取/寫入<br/> | 指定或抓取目標的 NetBIOS 名稱。<br/>                         |
| [**TargetPropertySet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | 讀取/寫入<br/> | 指定或抓取目標的屬性集。<br/>                        |
| [**TargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | 讀取/寫入<br/> | 指定或抓取目標狀態。<br/>                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                |
| 伺服器支援結束<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx 定義為74f99987-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[遠端桌面虛擬化介面](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 


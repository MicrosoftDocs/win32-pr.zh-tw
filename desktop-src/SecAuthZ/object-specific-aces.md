---
description: 目錄服務 (DS) 物件支援特定物件的 Ace。 特定物件的 ACE 包含一組 Guid，可擴充 ACE 可以保護物件的方式。
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: 物件特定的 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4212a0f7fe4eff7e38b41fe2636643c457cfeb51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469575"
---
# <a name="object-specific-aces"></a>物件特定的 Ace

目錄服務 (DS) 物件支援特定物件的 [*ace*](/windows/desktop/SecGloss/a-gly) 。 特定物件的 ACE 包含一組 Guid，可擴充 ACE 可以保護物件的方式。




| GUID | Description | 
|------|-------------|
| <strong>ObjectType</strong> | 識別下列其中一項：<ul><li>子物件的類型。 ACE 控制建立指定之子物件類型的許可權。 如需詳細資訊，請參閱 <a href="controlling-child-object-creation-in-c--.md">在 c + + 中控制建立子物件</a>。</li><li>屬性集或屬性。 ACE 控制讀取或寫入屬性（property）或屬性集的許可權。 如需詳細資訊，請參閱 <a href="aces-to-control-access-to-an-object-s-properties.md">ace 來控制物件屬性的存取</a>。</li><li>延伸的許可權。 ACE 控制執行與擴充許可權相關聯之作業的許可權。</li><li>經過驗證的寫入。 ACE 控制執行特定寫入作業的許可權。 這些已驗證的寫入權限（定義和公開于 ACL 編輯器中）提供了已驗證的屬性寫入權限，而不是針對以「寫入屬性」許可權授與的屬性進行未檢查的低層級寫入。</li></ul> | 
| <strong>InheritedObjectType</strong> | 表示可以繼承 ACE 的子物件類型。 繼承也是由 <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>中的繼承旗標，以及針對子物件所放置之繼承的任何保護所控制。 如需詳細資訊，請參閱 <a href="ace-inheritance.md">ACE 繼承</a>。 | 




 

支援三種類型的物件特定 Ace。

> [!Note]  
> 目前不支援系統警示物件 Ace。

 



| 類型                      | Description                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 拒絕存取的物件 ACE  | 用於 DACL 中，以拒絕受信任者存取物件上設定的屬性或屬性，或限制 ACE 繼承到指定的子物件類型。 使用 [**拒絕存取 \_ \_ 物件 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) 結構。         |
| 存取-允許的物件 ACE | 在 DACL 中用來允許信任者存取物件上設定的屬性或屬性，或限制 ACE 繼承至指定的子物件類型。 使用 [**存取 \_ 允許的 \_ 物件 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) 結構。      |
| 系統審核物件 ACE   | 在 SACL 中用來記錄受信任者嘗試存取物件上設定的屬性或屬性，或限制 ACE 繼承至指定的子物件類型。 使用 [**系統 \_ AUDIT \_ OBJECT \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) 結構。 |



 

任何包含物件專屬 ACE 的 ACL，都必須使用修訂 ACL 的 \_ 修訂 \_ DS。

 

 

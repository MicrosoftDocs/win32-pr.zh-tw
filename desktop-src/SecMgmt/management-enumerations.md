---
description: 列出 LSA 原則管理函數使用的列舉。
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: 安全性管理列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf87e6c41cb3e687a8927c294fe3bc1433a294aaf48991310b1c230f4741f299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894454"
---
# <a name="security-management-enumerations"></a>安全性管理列舉

安全性管理列舉包含下列各項：

-   [LSA 原則列舉](#lsa-policy-enumerations)
-   [更安全的列舉](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>LSA 原則列舉

LSA 原則管理函數會使用下列列舉類型。



| 列舉型別                                                                               | 描述                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**原則 \_ 審核 \_ 事件 \_ 類型**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | 定義系統可以審核的事件種類。                                                                                     |
| [**原則 \_ 資訊 \_ 類別**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | 定義可以設定或查詢 [**原則**](policy-object.md) 物件的資訊類型。                             |
| [**原則 \_ LSA \_ 伺服器 \_ 角色**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | 指出 LSA 伺服器的角色。                                                                                                   |
| [**原則 \_ 通知 \_ 資訊 \_ 類別**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | 定義您的應用程式可以要求變更通知的原則資訊和原則網域資訊類型。 |
| [**原則 \_ 伺服器 \_ 啟用 \_ 狀態**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | 代表 LSA 伺服器的狀態，也就是啟用或停用。                                                   |
| [**受信任的 \_ 資訊 \_ 類別**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | 定義可以針對受信任的網域設定或查詢的資訊類型。                                                     |



 

## <a name="safer-enumerations"></a>更安全的列舉

[更安全](safer.md) 地使用下列列舉類型。



| Name                                                               | 描述                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**更安全的 \_ 識別 \_ 類型**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | 列舉類型，定義可由 [**更安全的 \_ 識別 \_ 標頭**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) 結構識別的識別規則結構的可能類型。 |
| [**更安全的 \_ 物件 \_ 資訊 \_ 類別**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | 列舉類型，定義針對較安全物件所要求的資訊類型。                                                                                                            |
| [**更安全的 \_ 原則 \_ 資訊 \_ 類別**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | 列舉類型，定義可以查詢原則的方式。                                                                                                                         |



 

 

 




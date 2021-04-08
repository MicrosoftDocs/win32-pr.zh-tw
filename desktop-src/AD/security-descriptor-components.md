---
title: 安全描述項元件
description: 使用 IADs 取得方法來取出 IADsSecurityDescriptor 介面指標，您可以使用 IADsSecurityDescriptor 屬性來讀取或寫入目錄物件之安全描述項的元件。
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- 安全性描述項元件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef87b0e23f60fdbb4d0b03b421012d5918ed3c83
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681638"
---
# <a name="security-descriptor-components"></a>安全描述項元件

使用 [**IADs 取得**](/windows/desktop/api/iads/nf-iads-iads-get) 方法來取出 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面指標，您可以使用 **IADsSecurityDescriptor** 屬性來讀取或寫入目錄物件之安全描述項的元件。 例如，若要取得或設定物件的 DACL，請使用 [**objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 屬性。

安全描述項可以儲存下列資料：

-   識別物件擁有者的安全識別碼 (SID) ：物件的擁有者具有在物件的安全描述項中修改 DACL 和擁有者資料的隱含許可權。
-    (DACL) 的任意存取控制清單，識別可對物件執行各種作業的使用者和群組： DACL 包含存取控制專案清單 (Ace) 。 每個 ACE 都允許或拒絕指定之使用者帳戶、群組帳戶或其他受信任者的指定存取權限集。 如需詳細資訊，請參閱 [取出物件的 DACL](retrieving-an-objectampaposs-dacl.md)。
-   系統存取控制清單 (SACL) ，可控制系統如何嘗試存取物件： SACL 中的每個 ACE 都會指定針對指定的使用者帳戶、群組帳戶或其他信任者產生審核記錄專案的存取嘗試類型。 如需詳細資訊，請參閱 [取出物件的 SACL](retrieving-an-objectampaposs-sacl.md)。
-   一組 **安全性 \_ 描述項 \_ 控制** 旗標，可限定安全描述項或其元件的意義：例如， **SE \_ DACL \_ PROTECTED** 旗標會保護安全描述項的 DACL，使其無法繼承其父物件的 ace。
-   識別物件主要群組 (SID) 的安全識別碼： Active Directory Domain Services 不使用此元件。

如需可用來讀取和顯示物件安全描述項和 DACL 中資料的詳細資訊和程式碼範例，請參閱 [讀取物件的安全描述項](reading-an-objectampaposs-security-descriptor.md)。

 

 
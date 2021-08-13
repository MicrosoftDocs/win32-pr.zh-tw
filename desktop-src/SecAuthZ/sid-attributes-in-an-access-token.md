---
description: 存取權杖中 (SID) 的每個使用者和群組安全識別碼都有一組屬性，可控制系統在存取檢查中使用 SID 的方式。 下表列出控制存取檢查的屬性。
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: 存取權杖中的 SID 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe504e190e6d6e884b8068eb23983b2bc506c7c8447a8db77fd3ddb9cdfb917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413418"
---
# <a name="sid-attributes-in-an-access-token"></a>存取權杖中的 SID 屬性

[*存取權杖*](/windows/desktop/SecGloss/a-gly)中 (sid) 的每個使用者和群組 [*安全識別碼*](/windows/desktop/SecGloss/s-gly)都有一組屬性，可控制系統在存取檢查中使用 SID 的方式。 下表列出控制存取檢查的屬性。



| 屬性                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SE \_群組 \_ 已啟用              | 啟用此屬性的 SID 可進行存取檢查。 當系統執行存取檢查時，它會檢查是否有存取允許和拒絕存取的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 套用至存取權杖中其中一個已啟用的 sid。 除非設定了 SE \_ 群組 \_ 使用 [ \_ \_ \_ 僅限拒絕] 屬性，否則在存取檢查期間會忽略沒有這個屬性的 SID。<br/> |
| SE \_群組 \_ \_ 僅用於 \_ 拒絕 \_ | 具有這個屬性的 SID 是僅限拒絕的 SID。 當系統執行存取檢查時，它會檢查套用至 SID 的拒絕存取的 Ace，但會忽略 SID 的存取允許 Ace。 如果設定這個屬性， \_ \_ 就不會設定 SE GROUP ENABLED 屬性，也無法重新啟用 SID。<br/>                                                                                                                                                          |



 

若要設定或清除 \_ 群組 SID 的 [已啟用 SE 群組] \_ 屬性，請使用 [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)函數。 您無法停用具有 SE \_ 群組強制屬性的群組 SID \_ 。 您無法使用 **AdjustTokenGroups** 來停用存取權杖的使用者 SID。

若要判斷是否已在權杖中啟用 SID，也就是是否已啟用 SE \_ 群組的 \_ 屬性，請呼叫 [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)函數。

若要將 SE \_ 群組 \_ 用於 \_ SID 的 [ \_ \_ 僅限拒絕] 屬性，請在您呼叫 [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)函式時指定的僅限拒絕 sid 清單中包含 sid。 **CreateRestrictedToken** 可將 [ \_ 僅限拒絕] 屬性的 SE 群組套用 \_ \_ \_ \_ 至任何 SID，包括具有 SE \_ 群組強制屬性的使用者 SID 和群組 sid \_ 。 不過，您無法從 SID 移除僅限拒絕的屬性，也不能使用 [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)來設定 \_ \_ 僅限拒絕 SID 上的 SE 群組啟用屬性。

若要取得 SID 的屬性，請使用 TokenGroups 值來呼叫 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 函數。 此函式會傳回 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) 結構的陣列，以識別群組 sid 和其屬性。

 


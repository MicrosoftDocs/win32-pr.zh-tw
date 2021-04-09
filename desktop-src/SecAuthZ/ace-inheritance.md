---
description: 物件 ACL 可以包含它從其父容器繼承的 Ace。
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: ACE 繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943980"
---
# <a name="ace-inheritance"></a>ACE 繼承

物件的 ACL 可以包含繼承自其父容器的 Ace。 例如，登錄子機碼可以從登錄階層中其上方的金鑰繼承 Ace。 同樣地，NTFS 檔案系統中的檔案可以從包含它的目錄繼承 Ace。

ACE 的 [**ace \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header) 結構包含一組繼承旗標，這些旗標可控制 ace 繼承以及它附加之物件上的 ace 效果。 系統會根據 [ACE 繼承的規則](ace-inheritance-rules.md)，來解讀繼承旗標和其他繼承資訊。

下列功能已增強這些規則：

-   支援可 [繼承 ace 的自動傳播](automatic-propagation-of-inheritable-aces.md)。
-   區分直接套用至物件之繼承 Ace 和 Ace 的旗標。
-   物件特定的 Ace，可讓您指定可繼承 ACE 的子物件類型。
-   藉由在 \_ \_ \_ \_ [*安全描述項的*](/windows/desktop/SecGloss/s-gly) 控制位（系統 \_ 資源 \_ 屬性 \_ ACE 和系統 \_ 範圍 \_ 原則 \_ 識別碼 \_ ACE 除外）中設定 se DACL protected 或 se 受保護的位，來防止 DACL 或 SACL 繼承 ace。

 

 

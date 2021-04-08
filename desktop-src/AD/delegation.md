---
title: 委派
description: 委派是 Active Directory Domain Services 的最重要安全性功能之一。
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- 委派廣告
- 安全性廣告，委派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931899"
---
# <a name="delegation"></a>委派

*委派* 是 Active Directory Domain Services 的最重要安全性功能之一。 委派可讓更高的系統管理授權單位將容器和子樹的特定系統管理許可權授與個人和群組。 您不再需要網域系統管理員（具有大量使用者的廣泛授權）。

ACE 可以將容器中物件的特定系統管理許可權授與使用者或群組。 使用容器 ACL 中的 Ace，授與特定物件類別上特定作業的許可權。 例如，若要讓名為 "user 1" 的使用者成為「公司帳戶處理」組織單位的系統管理員，請在「公司帳戶處理」的 ACL 中新增 Ace，如下所示：

「使用者1」;准許建立、修改、刪除、物件類別使用者 "User 1";准許建立、修改、刪除、物件類別群組「使用者1」;准許Write; 物件類別使用者;屬性密碼 "

現在，使用者1可以在公司帳戶處理中建立新的使用者和群組，並在現有的使用者上設定密碼，但使用者1無法建立任何其他的物件類別，也無法影響任何其他容器中的使用者，除非當然，使用者1被授與其他容器的 Ace 存取權。

 

 





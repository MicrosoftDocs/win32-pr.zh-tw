---
description: 對等身分識別管理員 API 可讓您在對等應用程式中建立、列舉和操作對等身分識別。
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: 關於 Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849319"
---
# <a name="about-identity-manager"></a>關於 Identity Manager

對等身分識別管理員 API 可讓您在對等應用程式中建立、列舉和操作對等身分識別。 您可以使用使用此 API 所建立的對等身分識別，做為對等群組和對等名稱解析通訊協定的輸入， (PNRP) 命名空間提供者 Api。

## <a name="peer-identity-manager-best-practices"></a>對等身分識別管理員的最佳作法

每個使用者都應該有一些可用於對等活動的對等身分識別。 例如，使用者可能有兩個對等身分識別可用於工作和休閒。

設計完善的對等應用程式可讓使用者選取要使用的對等身分識別。 如果沒有任何現有的對等身分識別適合與應用程式搭配使用，則使用者可以建立新的對等身分識別。

設計完善的對等應用程式也會控制其所建立的身分識別數目。 如果應用程式建立暫時性對等身分識別，則應用程式必須在不需要身分識別時刪除對等身分識別。 如果應用程式未執行此維護，對等身分識別管理員可能會在移除某些對等身分識別之前，無法建立對等身分識別。

 

 




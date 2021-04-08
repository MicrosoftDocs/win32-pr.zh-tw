---
description: 以 Windows 為基礎的系統可以有多個 TrustedDomain 物件類型的實例。
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: TrustedDomain 物件類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690107"
---
# <a name="the-trusteddomain-object-type"></a>TrustedDomain 物件類型

以 Windows 為基礎的系統可以有多個 [**TrustedDomain**](trusteddomain-object.md) 物件類型的實例。 **TrustedDomain** 物件具有兩個在所有 **TrustedDomain** 物件中都必須是唯一的欄位：

-   [ **TrustedDomain** 的名稱](trusteddomain-object.md)
-   [**TrustedDomain**](trusteddomain-object.md)的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 。

嘗試使用已由另一個 **TrustedDomain** 物件使用的名稱或 SID 來建立新的 **TrustedDomain** 物件，將會遭到拒絕。

 

 

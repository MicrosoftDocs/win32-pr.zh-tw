---
description: 說明如何保護帳戶物件。
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: 帳戶物件保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49610827c8f27b2ad1dd645faca1374534b9d4acb8353421fc55901da724dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969757"
---
# <a name="account-object-protection"></a>帳戶物件保護

[**帳戶**](account-object.md) 物件會以下列方式受到保護：

-   群組 **世界** 具有一般 \_ 執行。
-   群組 **本機系統 \_ 管理員** 具有 DELETE、GENERIC \_ READ、generic \_ WRITE、generic \_ EXECUTE 和 WRITE \_ DACL 存取權。
-   群組 **本機系統 \_ 管理員** 會被指派為帳戶物件的擁有者和主要群組。

 

 




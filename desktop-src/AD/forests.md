---
title: 樹系
description: 樹系是一組未形成連續命名空間的一或多個域樹。
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- 樹系 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933068"
---
# <a name="forests"></a>樹系

[*樹*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85))系是一組未形成連續命名空間的一或多個域樹。 樹系中的所有樹狀結構都會共用通用的架構、設定和通用類別目錄。 指定樹系中的所有樹狀結構會根據可轉移的階層式 Kerberos 信任關係進行信任。 不同于樹狀結構，樹系不需要相異的名稱。 樹系以一組交互參考物件和 Kerberos 信任關係的形式存在於成員樹狀結構中。 樹系中的樹狀目錄會形成 Kerberos 信任用途的階層;信任樹狀結構根目錄中的樹狀結構名稱是指指定的樹系。

下圖顯示非連續命名空間的樹系。

![非連續命名空間的樹系](images/forests.png)

 

 
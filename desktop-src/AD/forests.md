---
title: 樹系
description: 樹系是一組未形成連續命名空間的一或多個域樹。
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- 樹系 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ccccbce1c660c3f1e185e75971aa71d613c2db012ce42979cfaee7cd9c2b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189200"
---
# <a name="forests"></a>樹系

[*樹*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85))系是一組未形成連續命名空間的一或多個域樹。 樹系中的所有樹狀結構都會共用通用的架構、設定和通用類別目錄。 指定樹系中的所有樹狀結構會根據可轉移的階層式 Kerberos 信任關係進行信任。 不同于樹狀結構，樹系不需要相異的名稱。 樹系以一組交互參考物件和 Kerberos 信任關係的形式存在於成員樹狀結構中。 樹系中的樹狀目錄會形成 Kerberos 信任用途的階層;信任樹狀結構根目錄中的樹狀結構名稱是指指定的樹系。

下圖顯示非連續命名空間的樹系。

![非連續命名空間的樹系](images/forests.png)

 

 
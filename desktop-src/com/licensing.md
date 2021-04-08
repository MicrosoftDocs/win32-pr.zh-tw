---
title: 授權
description: 授權
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683157"
---
# <a name="licensing"></a>授權

為了成功內嵌授權的控制項，ActiveX 控制項容器必須使用 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) ，而不是 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)。 有幾個 OLE 建立和載入 helper 函式 ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) 和 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) 明確地呼叫 **IClassFactory** 而不是 **IClassFactory2**，因此不能用來建立或載入授權的 ActiveX 控制項。 ActiveX 控制項容器應使用 **IClassFactory2** 來明確建立和載入 activex 控制項。

 

 
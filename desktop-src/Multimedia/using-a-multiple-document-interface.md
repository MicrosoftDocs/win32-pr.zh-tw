---
title: 使用多重文件介面
description: 使用多重文件介面
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941053"
---
# <a name="using-a-multiple-document-interface"></a>使用多重文件介面

使用多個檔介面 (MDI) 的應用程式可能需要指定無法透過 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函數使用的視窗樣式。 針對這些應用程式，您可以使用 [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) 函數搭配 [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來註冊和建立 MCIWnd 視窗。 **MCIWndRegisterClass** 函式會註冊 MCIWND \_ 視窗 \_ 類別視窗類別，然後 **CreateWindowEx** 會建立 MCIWND 視窗的實例。

 

 
---
title: 參考追蹤
description: 參考追蹤
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463741"
---
# <a name="reference-tracking"></a>參考追蹤

參考追蹤可以防止意外或惡意的物件早期發行版本。

當您啟用參考追蹤時，會要求由 COM 驗證分散式 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 呼叫。 啟用參考追蹤時，COM 會持續追蹤每個使用者的參考計數，讓使用者只能在使用者先前呼叫 **AddRef** 的物件上呼叫 **Release** 。 雖然參考追蹤可能會降低效能，但這可確保不論指定的使用者呼叫 **釋放** 多少次，如果其他人有參考，物件和存根仍會存在。

用戶端可以藉由 \_ \_ 在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫中傳遞 EOAC SECURE REFS 功能旗標，來設定進程的參考追蹤。 您也可以使用 Dcomcnfg.exe 來啟用或停用電腦上所有應用程式的參考追蹤。

如果已啟用參考追蹤， [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 一律會使用預設安全性設定。 在此情況下，對 **IUnknown** 的 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)呼叫會失敗。

 

 
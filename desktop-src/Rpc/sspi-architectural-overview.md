---
title: SSPI 架構總覽
description: SSPI 是軟體介面。
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023822"
---
# <a name="sspi-architectural-overview"></a>SSPI 架構總覽

SSPI 是軟體介面。 分散式程式設計程式庫（例如 RPC）可以使用它來進行驗證通訊。 一或多個軟體模組提供實際的驗證功能。 每個模組（稱為安全性支援提供者 (SSP) ）會實作為動態連結程式庫 (DLL) 。 SSP 會提供一或多個安全性套件。

有各種不同的 Ssp 和套件可供使用。 Windows 隨附的是 NTLM 安全性套件和 Microsoft Kerberos 通訊協定安全性封裝。 此外，您可以選擇安裝安全通訊端層 (SSL) 安全性封裝，或任何其他與 SSPI 相容的 SSP。

使用 SSPI 可確保無論您選取哪一個 SSP，您的應用程式都能以一致的方式存取驗證功能。 這項功能可讓您的應用程式比過去所提供的網路更有更大的獨立性。

分散式應用程式會透過 RPC 介面進行通訊。 接著，RPC 軟體會透過 SSPI 存取 SSP 的驗證功能。

如需詳細資訊，請參閱 [SSPI](/windows/desktop/SecAuthN/sspi)。

 

 
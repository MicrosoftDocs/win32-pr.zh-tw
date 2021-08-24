---
description: 媒體服務提供者必須執行 MSPI 介面的最小子集 ITMSPAddress ITTerminalSupport ITStreamControl 和 ITStream。
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: 撰寫媒體服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f99cc8a52b7362caa01d9743fea7fc848faec2ae451b96ec916f4f3aa5c287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739018"
---
# <a name="writing-a-media-service-provider"></a>撰寫媒體服務提供者

媒體服務提供者必須執行 MSPI 介面的最小子集： [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)、 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)、 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)和 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)。 子流支援是選擇性的。 此外，指定的 MSP 也可以實行其他方法，例如特製化硬體所需的控制項。

下列材質檔：

-   [TAPI 3 MSP 基類](tapi-3-msp-base-classes.md)是一組 c + + 類別，其設計目的是要簡化建立以 DirectShow 為基礎之 MSP 的工作。 基類會以一般方式執行所有的 MSPI 介面。 不同的 Msp 可以覆寫 MSP 特定的函式，並提供自己的實作為。
-   [TAPI 3 終端機管理員](tapi-3-terminal-manager.md)，提供 MSP 用來控制終端機的介面和方法。
-   可[插入的終端](writing-a-pluggable-terminal.md)機，可允許應用程式而非 MSP 來建立終端機。 已經過撰寫服務提供者的開發人員，將會是插入式終端機的主要建立者。 針對此版本所執行的初始版本，是針對需要將非 Windows 2000 或非多播用戶端新增至 TAPI 3 多方 SDP/IP 多播會議的會議服務器應用程式。

 

 

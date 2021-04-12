---
description: 媒體服務提供者必須執行 MSPI 介面的最小子集 ITMSPAddress ITTerminalSupport ITStreamControl 和 ITStream。
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: 撰寫媒體服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321443"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="583ec-103">撰寫媒體服務提供者</span><span class="sxs-lookup"><span data-stu-id="583ec-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="583ec-104">媒體服務提供者必須執行 MSPI 介面的最小子集： [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)、 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)、 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)和 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)。</span><span class="sxs-lookup"><span data-stu-id="583ec-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="583ec-105">子流支援是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="583ec-105">SubStream support is optional.</span></span> <span data-ttu-id="583ec-106">此外，指定的 MSP 也可以實行其他方法，例如特製化硬體所需的控制項。</span><span class="sxs-lookup"><span data-stu-id="583ec-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="583ec-107">下列材質檔：</span><span class="sxs-lookup"><span data-stu-id="583ec-107">The following material documents:</span></span>

-   <span data-ttu-id="583ec-108">[TAPI 3 MSP 基礎類別](tapi-3-msp-base-classes.md)是一組 c + + 類別，其設計目的是要簡化建立 DIRECTSHOW 型 MSP 的工作。</span><span class="sxs-lookup"><span data-stu-id="583ec-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="583ec-109">基類會以一般方式執行所有的 MSPI 介面。</span><span class="sxs-lookup"><span data-stu-id="583ec-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="583ec-110">不同的 Msp 可以覆寫 MSP 特定的函式，並提供自己的實作為。</span><span class="sxs-lookup"><span data-stu-id="583ec-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="583ec-111">[TAPI 3 終端機管理員](tapi-3-terminal-manager.md)，提供 MSP 用來控制終端機的介面和方法。</span><span class="sxs-lookup"><span data-stu-id="583ec-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="583ec-112">可[插入的終端](writing-a-pluggable-terminal.md)機，可允許應用程式而非 MSP 來建立終端機。</span><span class="sxs-lookup"><span data-stu-id="583ec-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="583ec-113">已經過撰寫服務提供者的開發人員，將會是插入式終端機的主要建立者。</span><span class="sxs-lookup"><span data-stu-id="583ec-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="583ec-114">此版本所執行的初始版本是針對需要將非 Windows 2000 或非多播用戶端新增至 TAPI 3 多方 SDP/IP 多播會議的會議服務器應用程式。</span><span class="sxs-lookup"><span data-stu-id="583ec-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 

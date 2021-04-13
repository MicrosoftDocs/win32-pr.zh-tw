---
description: " (MSP 的 TAPI 3 媒體服務提供者) 可讓應用程式對特定傳輸機制的媒體具有相當大的控制權。"
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: '關於媒體服務提供者 (MSP) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116037"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="a2c66-103">關於媒體服務提供者 (MSP) </span><span class="sxs-lookup"><span data-stu-id="a2c66-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="a2c66-104"> (MSP 的 TAPI 3 媒體服務提供者) 可讓應用程式對特定傳輸機制的媒體具有相當大的控制權。</span><span class="sxs-lookup"><span data-stu-id="a2c66-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="a2c66-105">MSP 永遠存在，與電話語音服務提供者 (TSP) 配對。</span><span class="sxs-lookup"><span data-stu-id="a2c66-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="a2c66-106">如同 TSP 是用於呼叫控制的抽象層，MSP 可控制媒體，而不需要裝置特定的程式碼撰寫。</span><span class="sxs-lookup"><span data-stu-id="a2c66-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="a2c66-107">如需 MSP/TSP 通訊的範例，請參閱 [TAPI 服務提供者總覽](./tapi-service-provider-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="a2c66-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="a2c66-108">MSP 利用 TAPI 所定義的特殊終端機、串流和子資料流程介面，讓媒體控制。</span><span class="sxs-lookup"><span data-stu-id="a2c66-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="a2c66-109">[關於通話和媒體控制項](about-call-and-media-controls.md)的圖表說明這些介面如何顯示在 TAPI 3 應用程式中。</span><span class="sxs-lookup"><span data-stu-id="a2c66-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="a2c66-110">此外，MSP 可能會執行私用 [提供者特定的介面](provider-specific-interfaces.md)，而 TAPI 會匯總到公開給應用程式的標準物件。</span><span class="sxs-lookup"><span data-stu-id="a2c66-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="a2c66-111">例如，Microsoft IPConf MSP （與 Microsoft Windows 2000 一起安裝）會執行 [**ITParticipant**](itparticipant.md) 介面，此介面會提供會議個別成員的控制項。</span><span class="sxs-lookup"><span data-stu-id="a2c66-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="a2c66-112">下列主題簡要說明可能與 Microsoft 作業系統一起安裝的 Msp。</span><span class="sxs-lookup"><span data-stu-id="a2c66-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="a2c66-113">如需設定和使用方式的詳細資訊，請參閱目標平臺的資源套件。</span><span class="sxs-lookup"><span data-stu-id="a2c66-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="a2c66-114">其他協力廠商媒體服務提供者可以針對特定的通訊協定或實體裝置來撰寫。</span><span class="sxs-lookup"><span data-stu-id="a2c66-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="a2c66-115">[媒體服務提供者介面 (MSPI) ](media-service-provider-interface-mspi-.md)說明必須執行的介面，才能讓 MSP 與 Microsoft 電話語音的元件互動。</span><span class="sxs-lookup"><span data-stu-id="a2c66-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 

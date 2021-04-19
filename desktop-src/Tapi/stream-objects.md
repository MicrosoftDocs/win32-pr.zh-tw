---
description: 資料流程物件是與呼叫會話相關聯之媒體資料流程或資料流程的抽象概念。
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: 資料流程物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979898"
---
# <a name="stream-objects"></a><span data-ttu-id="2d43c-103">資料流程物件</span><span class="sxs-lookup"><span data-stu-id="2d43c-103">Stream Objects</span></span>

<span data-ttu-id="2d43c-104">資料流程物件是與呼叫會話相關聯之媒體資料流程或資料流程的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="2d43c-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="2d43c-105">在 stream 和子資料流程物件上公開的介面和方法可讓應用程式執行非常詳細的控制項，例如暫停串流、將新的媒體類型新增至通訊會話，或調整特定會議參與者的音訊音量。</span><span class="sxs-lookup"><span data-stu-id="2d43c-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="2d43c-106">資料流程和子資料流程是資料流程的兩種主要類型。</span><span class="sxs-lookup"><span data-stu-id="2d43c-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="2d43c-107">標準執行的介面和方法類似于兩者，但 substreaming 允許較低層級的控制。</span><span class="sxs-lookup"><span data-stu-id="2d43c-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="2d43c-108"> (Msp) 的所有媒體服務提供者都必須執行基本的資料流程控制介面，但支援子串流是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2d43c-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="2d43c-109">此外，某些服務提供者會為數據流執行 [提供者特定的介面](provider-specific-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d43c-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="2d43c-110">例如，IPConf MSP 提供參與者層級的控制項。</span><span class="sxs-lookup"><span data-stu-id="2d43c-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="2d43c-111">如需摘要，請參閱 [IPCONF MSP 介面](ipconf-msp-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d43c-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="2d43c-112">如需其他可能會執行的介面，請參閱服務提供者的檔。</span><span class="sxs-lookup"><span data-stu-id="2d43c-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="2d43c-113">MSP 和 TAPI 會在初始設定傳出或傳入會話的期間，建立用於呼叫的資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="2d43c-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="2d43c-114">應用程式會負責識別這些資料流程的適當終端機，並選取終端機至資料流程。</span><span class="sxs-lookup"><span data-stu-id="2d43c-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="2d43c-115">請注意，在某些情況下，MSP 可能會要求應用程式在特定呼叫會話作業之前停止或暫停串流。</span><span class="sxs-lookup"><span data-stu-id="2d43c-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="2d43c-116">串流介面記載于 [媒體服務提供者介面 (MSPI) 參考](media-service-provider-interface-mspi-reference.md)中。</span><span class="sxs-lookup"><span data-stu-id="2d43c-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="2d43c-117">[選取終端](select-a-terminal.md)機程式碼範例會示範如何列舉資料流程，以及如何在其上選取終端機。</span><span class="sxs-lookup"><span data-stu-id="2d43c-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 




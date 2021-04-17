---
description: 所有虛擬機器都反映出模擬的 S3 影片控制器以及加速的綜合視訊控制器。
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: 影片類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469433"
---
# <a name="video-classes"></a><span data-ttu-id="158ce-103">影片類別</span><span class="sxs-lookup"><span data-stu-id="158ce-103">Video classes</span></span>

<span data-ttu-id="158ce-104">所有虛擬機器都反映出模擬的 S3 影片控制器以及加速的綜合視訊控制器。</span><span class="sxs-lookup"><span data-stu-id="158ce-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="158ce-105">每個顯示控制器都有與其相關聯的影片標頭物件。</span><span class="sxs-lookup"><span data-stu-id="158ce-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="158ce-106">虛擬機器中隨時只能有一個顯示控制器處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="158ce-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="158ce-107">連接至虛擬機器的每個作用中遠端會話都有一個終端機連線。</span><span class="sxs-lookup"><span data-stu-id="158ce-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="158ce-108">以下是與影片相關的虛擬化 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="158ce-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="158ce-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="158ce-109">In this section</span></span>



| <span data-ttu-id="158ce-110">主題</span><span class="sxs-lookup"><span data-stu-id="158ce-110">Topic</span></span>                                                                                  | <span data-ttu-id="158ce-111">描述</span><span class="sxs-lookup"><span data-stu-id="158ce-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="158ce-112">**Msvm \_ S3DisplayController**</span><span class="sxs-lookup"><span data-stu-id="158ce-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="158ce-113">代表存在於每個虛擬機器設定中的模擬 S3 控制器的狀態。</span><span class="sxs-lookup"><span data-stu-id="158ce-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="158ce-114">**Msvm \_ SyntheticDisplayController**</span><span class="sxs-lookup"><span data-stu-id="158ce-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="158ce-115">代表存在於每個虛擬機器設定中的綜合顯示控制器的狀態。</span><span class="sxs-lookup"><span data-stu-id="158ce-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="158ce-116">**Msvm \_ SystemTerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="158ce-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="158ce-117">將虛擬機器與終端機連線建立關聯。</span><span class="sxs-lookup"><span data-stu-id="158ce-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="158ce-118">**Msvm \_ TerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="158ce-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="158ce-119">表示與虛擬機器互動之作用中遠端會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="158ce-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="158ce-120">**Msvm \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="158ce-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="158ce-121">描述顯示控制器上的主要繪圖介面。</span><span class="sxs-lookup"><span data-stu-id="158ce-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="158ce-122">**Msvm \_ VideoHeadOnController**</span><span class="sxs-lookup"><span data-stu-id="158ce-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="158ce-123">將影片標頭與包含它的影片控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="158ce-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 





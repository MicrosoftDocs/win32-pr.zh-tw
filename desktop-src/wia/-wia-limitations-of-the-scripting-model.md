---
description: 深入瞭解：腳本模型的限制
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: 腳本模型的限制
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986356"
---
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="09403-103">腳本模型的限制</span><span class="sxs-lookup"><span data-stu-id="09403-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="09403-104">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="09403-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="09403-105">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="09403-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="09403-106">Windows 映像取得 (WIA) 腳本模型會公開 WIA 功能的子集。</span><span class="sxs-lookup"><span data-stu-id="09403-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="09403-107">下表提供腳本模型的限制描述。</span><span class="sxs-lookup"><span data-stu-id="09403-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="09403-108">WIA 功能</span><span class="sxs-lookup"><span data-stu-id="09403-108">WIA Functionality</span></span>               | <span data-ttu-id="09403-109">腳本模型限制</span><span class="sxs-lookup"><span data-stu-id="09403-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09403-110">隱藏使用者介面</span><span class="sxs-lookup"><span data-stu-id="09403-110">Suppressing the user interface</span></span>  | <span data-ttu-id="09403-111">無法隱藏設定裝置/傳輸屬性的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="09403-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="09403-112">設定屬性</span><span class="sxs-lookup"><span data-stu-id="09403-112">Setting properties</span></span>              | <span data-ttu-id="09403-113">無法將 (寫入) 任何裝置或專案屬性。</span><span class="sxs-lookup"><span data-stu-id="09403-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="09403-114">註冊回呼事件</span><span class="sxs-lookup"><span data-stu-id="09403-114">Registering for callback events</span></span> | <span data-ttu-id="09403-115">只能接收三個指定事件的通知： [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)、 [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)和 [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md)。</span><span class="sxs-lookup"><span data-stu-id="09403-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="09403-116">處理錯誤</span><span class="sxs-lookup"><span data-stu-id="09403-116">Handling errors</span></span>                 | <span data-ttu-id="09403-117">無法處理 WIA 錯誤。</span><span class="sxs-lookup"><span data-stu-id="09403-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 

---
description: 專用通訊硬體（例如纜線數據機或電話語音卡）通常會使用一或多個裝置專用的 Tsp 和 Msp。 裝置的檔應該指出功能並提供程式設計指導方針。
ms.assetid: 9033b651-c8f4-47f1-b953-557b519ea3bc
title: 協力廠商 TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee3c658d549eba384af4e71d7f59d62f4630a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996728"
---
# <a name="third-party-tsp"></a><span data-ttu-id="648e9-104">協力廠商 TSP</span><span class="sxs-lookup"><span data-stu-id="648e9-104">Third-Party TSP</span></span>

<span data-ttu-id="648e9-105">專用通訊硬體（例如纜線數據機或電話語音卡）通常會使用一或多個裝置專用的 Tsp 和 Msp。</span><span class="sxs-lookup"><span data-stu-id="648e9-105">Specialized communications hardware such as cable modems or telephony cards typically arrive with one or more TSPs and MSPs specific to the device.</span></span> <span data-ttu-id="648e9-106">裝置的檔應該指出功能並提供程式設計指導方針。</span><span class="sxs-lookup"><span data-stu-id="648e9-106">Documentation for the device should indicate capabilities and give programming guidelines.</span></span>

<span data-ttu-id="648e9-107">如果舊版 TSP 沒有 MSP，但卻使用 wave 裝置，TAPI 會將 Wave MSP 與該 TSP 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="648e9-107">If a legacy TSP does not have an MSP but does use wave devices, TAPI will associate the Wave MSP with that TSP.</span></span> <span data-ttu-id="648e9-108">未使用 wave 裝置的舊版 Tsp 將不會被指派相關聯的 MSP，也無法使用串流控制作業。</span><span class="sxs-lookup"><span data-stu-id="648e9-108">Legacy TSPs that do not use wave devices will not be assigned an associated MSP, and stream control operations will not be available.</span></span>

<span data-ttu-id="648e9-109">協力廠商 TSP 會隨其預定支援的裝置一起安裝。</span><span class="sxs-lookup"><span data-stu-id="648e9-109">A third-party TSP is installed with the device it is intended to support.</span></span>

 

 




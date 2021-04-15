---
description: 啟用筆墨的應用程式會透過 Tablet PC 平臺 Api 與辨識系統通訊。
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: 辨識 API 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554191"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="62835-103">辨識 API 架構</span><span class="sxs-lookup"><span data-stu-id="62835-103">Recognition API Architecture</span></span>

<span data-ttu-id="62835-104">啟用筆墨的應用程式會透過 Tablet PC 平臺 Api 與辨識系統通訊。</span><span class="sxs-lookup"><span data-stu-id="62835-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="62835-105">應用程式會使用 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件來完成此動作。</span><span class="sxs-lookup"><span data-stu-id="62835-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="62835-106">Tablet PC 平臺會使用本節所述的 C 樣式介面，與您的辨識器互動。</span><span class="sxs-lookup"><span data-stu-id="62835-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="62835-107">在下圖中，虛線內的區域會顯示本節所述的內容。</span><span class="sxs-lookup"><span data-stu-id="62835-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![已反白顯示辨識器的辨識架構圖例](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="62835-109">自訂辨識器必須包含預設安裝在 C： \\ Program Files \\ MICROSOFT Tablet PC Platform SDK 中的 Recapis (， \\ 包括) 。</span><span class="sxs-lookup"><span data-stu-id="62835-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="62835-110">除非另有說明，否則您的動態連結程式庫 (DLL) 必須匯出所有 API 函式，即使您選擇讓其中一部分傳回 E >notimpl 亦同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="62835-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="62835-111">在任何情況下，您的辨識器會直接由啟用筆墨的應用程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="62835-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="62835-112">相反地，應用程式會呼叫自動化 Api 或受控 Api，以從您的辨識器取得結果。</span><span class="sxs-lookup"><span data-stu-id="62835-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 




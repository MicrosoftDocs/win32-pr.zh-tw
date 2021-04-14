---
description: Tablet PC 有一個有趣的新功能，就是手寫筆的輸入系統。
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: 畫筆輸入、筆跡和辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568295"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="1b4cc-103">畫筆輸入、筆跡和辨識</span><span class="sxs-lookup"><span data-stu-id="1b4cc-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="1b4cc-104">Tablet PC 有一個有趣的新功能，就是手寫筆的輸入系統。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="1b4cc-105">所有 Tablet PC 電腦在畫面下方都有一個接受畫筆輸入的數位板。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="1b4cc-106">這種新的輸入機制需要您思考如何特別針對 Tablet PC 建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="1b4cc-107"> (API) 的 Tablet PC 平臺應用程式開發介面可協助您進行此作業。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="1b4cc-108">集合、資料管理和辨識</span><span class="sxs-lookup"><span data-stu-id="1b4cc-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="1b4cc-109">Tablet PC 平臺可以分成三個不同的區域：</span><span class="sxs-lookup"><span data-stu-id="1b4cc-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="1b4cc-110">筆墨集合 (用來從數位板) 收集筆墨的物件。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="1b4cc-111">筆墨資料管理 (用來管理所收集之筆墨) 的物件。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="1b4cc-112">筆跡辨識 (物件，用來將所收集的筆墨轉換成其他類型的資料，例如文字) 。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="1b4cc-113">下圖將概要說明 Tablet Collection API 如何 (畫筆 API) 、筆墨資料管理 API (筆墨 API) 和筆跡辨識 API (辨識 API) 在 Tablet PC 平臺中一起運作。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![顯示畫筆 api、筆墨 api 和辨識 api 如何一起運作的圖例](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="1b4cc-115">Tablet PC 平臺 API 適用于受控 Api 和 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="1b4cc-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="1b4cc-116">下列主題描述 API 中的物件，並說明應用程式如何使用這些物件：</span><span class="sxs-lookup"><span data-stu-id="1b4cc-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="1b4cc-117">筆墨集合</span><span class="sxs-lookup"><span data-stu-id="1b4cc-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="1b4cc-118">筆墨資料</span><span class="sxs-lookup"><span data-stu-id="1b4cc-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="1b4cc-119">筆跡辨識</span><span class="sxs-lookup"><span data-stu-id="1b4cc-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="1b4cc-120">筆墨分析</span><span class="sxs-lookup"><span data-stu-id="1b4cc-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="1b4cc-121">Windows Server 2008 R2 中的手寫辨識</span><span class="sxs-lookup"><span data-stu-id="1b4cc-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 




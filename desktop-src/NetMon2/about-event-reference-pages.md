---
description: " (ERP) 的事件參考頁面是一份 HTML 檔案，提供在專家或監視作業期間偵測到的事件網路監視器資訊。"
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: 關於事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849466"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="aa268-103">關於事件參考頁面</span><span class="sxs-lookup"><span data-stu-id="aa268-103">About Event Reference Pages</span></span>

<span data-ttu-id="aa268-104"> (ERP) 的事件參考頁面是一份 HTML 檔案，提供在專家或監視作業期間偵測到的事件網路監視器資訊。</span><span class="sxs-lookup"><span data-stu-id="aa268-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="aa268-105">您可以在網路監視器、監視器控制工具的事件檢視器中，或在支援 Microsoft Internet Explorer 4.01 版或更新版本之 HTML 功能的任何瀏覽器中，查看 ERPs。</span><span class="sxs-lookup"><span data-stu-id="aa268-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="aa268-106">也就是說，您可以將支援的控制項或指令碼語言新增至 ERP。</span><span class="sxs-lookup"><span data-stu-id="aa268-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="aa268-107">不過，只有當專家依名稱指定 HTML 檔案時，才會顯示 ERPs。</span><span class="sxs-lookup"><span data-stu-id="aa268-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="aa268-108">若已正確指定，當選取事件檢視器中的事件時，ERP 會出現在下方窗格中。</span><span class="sxs-lookup"><span data-stu-id="aa268-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="aa268-109">下圖顯示與網際網路通訊協定 (IP) 範圍監視相關聯的 ERP。</span><span class="sxs-lookup"><span data-stu-id="aa268-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![與 ip 範圍監視相關聯的 erp](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="aa268-111">專家活動</span><span class="sxs-lookup"><span data-stu-id="aa268-111">Expert Events</span></span>

<span data-ttu-id="aa268-112">專家活動是由 [**NMEVENTDATA**](nmeventdata.md)結構的 **EventIdent** 成員所識別。</span><span class="sxs-lookup"><span data-stu-id="aa268-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="aa268-113">當您撰寫專家時，會決定 **EventIdent** 值，通常是編號1、2、3等等。</span><span class="sxs-lookup"><span data-stu-id="aa268-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="aa268-114">例如，假設專家產生兩個事件 (**EventIdent1** 和 **EventIdent2**) 。</span><span class="sxs-lookup"><span data-stu-id="aa268-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="aa268-115">如果您想要讓事件檢視器分別顯示事件，您必須建立兩個不同的 ERP 檔。</span><span class="sxs-lookup"><span data-stu-id="aa268-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 




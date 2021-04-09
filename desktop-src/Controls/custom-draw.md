---
title: 自訂繪圖
description: 自訂繪製不是通用控制項;它是許多常見控制項所提供的服務。
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932015"
---
# <a name="custom-draw"></a><span data-ttu-id="e1301-103">自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="e1301-103">Custom Draw</span></span>

<span data-ttu-id="e1301-104">自訂繪製不是通用控制項;它是許多常見控制項所提供的服務。</span><span class="sxs-lookup"><span data-stu-id="e1301-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="e1301-105">自訂繪圖服務可讓應用程式更有彈性地自訂控制項的外觀。</span><span class="sxs-lookup"><span data-stu-id="e1301-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="e1301-106">您的應用程式可以利用自訂繪製通知，輕鬆地變更用來顯示專案或手動繪製專案的字型，而不需要進行完整的擁有者繪製。</span><span class="sxs-lookup"><span data-stu-id="e1301-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="e1301-107">本章節包含與自訂繪圖搭配使用之程式設計項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1301-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="e1301-108">概觀</span><span class="sxs-lookup"><span data-stu-id="e1301-108">Overviews</span></span>



| <span data-ttu-id="e1301-109">主題</span><span class="sxs-lookup"><span data-stu-id="e1301-109">Topic</span></span>                                      | <span data-ttu-id="e1301-110">目錄</span><span class="sxs-lookup"><span data-stu-id="e1301-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1301-111">關於自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="e1301-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="e1301-112">本章節包含有關自訂繪製功能的一般資訊，並提供應用程式如何支援自訂繪製的概念總覽。</span><span class="sxs-lookup"><span data-stu-id="e1301-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="e1301-113">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="e1301-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="e1301-114">本節包含示範如何執行自訂繪製的範例。</span><span class="sxs-lookup"><span data-stu-id="e1301-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="e1301-115">通知</span><span class="sxs-lookup"><span data-stu-id="e1301-115">Notifications</span></span>



| <span data-ttu-id="e1301-116">主題</span><span class="sxs-lookup"><span data-stu-id="e1301-116">Topic</span></span>                               | <span data-ttu-id="e1301-117">目錄</span><span class="sxs-lookup"><span data-stu-id="e1301-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1301-118">NM \_ CUSTOMDRAW</span><span class="sxs-lookup"><span data-stu-id="e1301-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="e1301-119">通知控制項的父視窗有關自訂繪圖作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1301-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="e1301-120">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e1301-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="e1301-121">結構</span><span class="sxs-lookup"><span data-stu-id="e1301-121">Structures</span></span>



| <span data-ttu-id="e1301-122">主題</span><span class="sxs-lookup"><span data-stu-id="e1301-122">Topic</span></span>                                | <span data-ttu-id="e1301-123">目錄</span><span class="sxs-lookup"><span data-stu-id="e1301-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1301-124">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="e1301-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="e1301-125">包含 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="e1301-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 






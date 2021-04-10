---
title: 開始開發 Windows 應用程式的 UI
description: .
ms.assetid: 29d6f67b-46fa-4f39-a319-306c832eff9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c3d1a182aef6354901f0fa71f94b39ecdc58f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682810"
---
# <a name="getting-started-developing-user-interfaces-for-windows-applications"></a><span data-ttu-id="29644-103">開發 Windows 應用程式的使用者介面開始使用</span><span class="sxs-lookup"><span data-stu-id="29644-103">Getting Started Developing User Interfaces for Windows Applications</span></span>

## <a name="purpose"></a><span data-ttu-id="29644-104">目的</span><span class="sxs-lookup"><span data-stu-id="29644-104">Purpose</span></span>

<span data-ttu-id="29644-105">下列各節針對設計、執行和測試 Windows 應用程式使用者介面的開發人員提供一般指引。</span><span class="sxs-lookup"><span data-stu-id="29644-105">The following sections offer general guidance to developers who are designing, implementing, and testing the user interface of a Windows application.</span></span>

<span data-ttu-id="29644-106">除了基本的使用者介面設計原則之外，還提供了許多建議和建議，可協助開發人員提供簡單、有效率且盡可能愉快的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="29644-106">In addition to basic user interface design principles, numerous recommendations and suggestions are provided that will help developers provide a user experience that is as simple, efficient, and enjoyable as possible.</span></span>

> [!Note]  
> <span data-ttu-id="29644-107">這些指導方針並不完整，且受限於應用程式的特定範圍和功能。</span><span class="sxs-lookup"><span data-stu-id="29644-107">These guidelines are not intended to be comprehensive and are subject to the specific scope and functionality of an application.</span></span> <span data-ttu-id="29644-108">如需更完整的指導方針，請參閱 [Windows 使用者經驗互動指導方針](../uxguide/guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="29644-108">For more comprehensive guidelines, see the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="29644-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="29644-109">In this section</span></span>



| <span data-ttu-id="29644-110">主題</span><span class="sxs-lookup"><span data-stu-id="29644-110">Topic</span></span>                                                                            | <span data-ttu-id="29644-111">描述</span><span class="sxs-lookup"><span data-stu-id="29644-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29644-112">消費者介面開發流程的總覽</span><span class="sxs-lookup"><span data-stu-id="29644-112">Overview of the User Interface Development Process</span></span>](the-process.md)<br/> | <span data-ttu-id="29644-113">本節將概述使用者介面設計的三個階段，並介紹通常與每個階段相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="29644-113">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span><br/>                                              |
| [<span data-ttu-id="29644-114">設計消費者介面</span><span class="sxs-lookup"><span data-stu-id="29644-114">Designing a User Interface</span></span>](designing-a-user-interface.md)<br/>          | <span data-ttu-id="29644-115">本節詳細說明一些與設計 Windows 應用程式之 UI 相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="29644-115">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span><br/>                                                                         |
| [<span data-ttu-id="29644-116">執行消費者介面</span><span class="sxs-lookup"><span data-stu-id="29644-116">Implementing a User Interface</span></span>](implementing-a-user-interface.md)<br/>    | <span data-ttu-id="29644-117">本節說明一些與執行 Windows 應用程式之使用者介面相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="29644-117">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span><br/>                                                                    |
| [<span data-ttu-id="29644-118">測試消費者介面</span><span class="sxs-lookup"><span data-stu-id="29644-118">Testing a User Interface</span></span>](testing-a-user-interface.md)<br/>              | <span data-ttu-id="29644-119">本節詳細說明一些與測試 Windows 應用程式的 UI 相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="29644-119">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span><br/>                                                                           |
| [<span data-ttu-id="29644-120">安全性考慮： Windows 消費者介面</span><span class="sxs-lookup"><span data-stu-id="29644-120">Security Considerations: Windows User Interface</span></span>](sec-ui.md)<br/>         | <span data-ttu-id="29644-121">本主題提供有關 Windows 消費者介面中安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="29644-121">This topic provides information about security considerations in the Windows User Interface.</span></span><br/>                                                                                         |
| [<span data-ttu-id="29644-122">其他資源</span><span class="sxs-lookup"><span data-stu-id="29644-122">Other Resources</span></span>](other-resources.md)<br/>                                | <span data-ttu-id="29644-123">本章節包含與使用者介面設計相關之建議書籍和資源的清單。</span><span class="sxs-lookup"><span data-stu-id="29644-123">This section contains a list of recommended books and resources related to user interface design.</span></span> <span data-ttu-id="29644-124">這些書籍和資源 (可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="29644-124">(These books and resources may not be available in some languages and countries.)</span></span> <br/> |



 

 


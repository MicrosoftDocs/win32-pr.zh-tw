---
title: '伺服器功能 (Windows 協助工具功能) '
description: 伺服器函數
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a747c073e84049fe578d19561b25d0b754dbb9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383778"
---
# <a name="server-functions-windows-accessibility-features"></a><span data-ttu-id="062aa-103">伺服器功能 (Windows 協助工具功能) </span><span class="sxs-lookup"><span data-stu-id="062aa-103">Server Functions (Windows Accessibility features)</span></span>

<span data-ttu-id="062aa-104">本章節包含與 Microsoft Active Accessibility 搭配使用之伺服器函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="062aa-104">This section contains information about the server functions used with Microsoft Active Accessibility.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="062aa-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="062aa-105">In this section</span></span>



| <span data-ttu-id="062aa-106">主題</span><span class="sxs-lookup"><span data-stu-id="062aa-106">Topic</span></span>                                                                     | <span data-ttu-id="062aa-107">描述</span><span class="sxs-lookup"><span data-stu-id="062aa-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="062aa-108">**AccNotifyTouchInteraction**</span><span class="sxs-lookup"><span data-stu-id="062aa-108">**AccNotifyTouchInteraction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | <span data-ttu-id="062aa-109">允許) 應用程式上的輔助技術 (，以透過 Windows 自動化 (API （例如 Microsoft 消費者介面自動化) 作為使用者觸控手勢的結果，來通知系統它正在與 UI 互動。</span><span class="sxs-lookup"><span data-stu-id="062aa-109">Allows an assistive technology (AT) application to notify the system that it is interacting with UI through a Windows Automation API (such as Microsoft UI Automation) as a result of a touch gesture from the user.</span></span> <span data-ttu-id="062aa-110">這可讓輔助技術通知目標應用程式，以及使用者要與觸控互動的系統。</span><span class="sxs-lookup"><span data-stu-id="062aa-110">This allows the assistive technology to notify the target application and the system that the user is interacting with touch.</span></span><br/> |
| [<span data-ttu-id="062aa-111">**AccSetRunningUtilityState**</span><span class="sxs-lookup"><span data-stu-id="062aa-111">**AccSetRunningUtilityState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | <span data-ttu-id="062aa-112">設定系統值，指出在) 應用程式目前狀態 (的輔助技術是否會影響通常由系統提供的功能。</span><span class="sxs-lookup"><span data-stu-id="062aa-112">Sets system values that indicate whether an assistive technology (AT) application's current state affects functionality that is typically provided by the system.</span></span> <br/>                                                                                                                                                                                 |
| [<span data-ttu-id="062aa-113">**CreateStdAccessibleObject**</span><span class="sxs-lookup"><span data-stu-id="062aa-113">**CreateStdAccessibleObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | <span data-ttu-id="062aa-114">使用指定之系統提供的使用者介面元素類型的方法和屬性，建立可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="062aa-114">Creates an accessible object with the methods and properties of the specified type of system-provided user interface element.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="062aa-115">**CreateStdAccessibleProxy**</span><span class="sxs-lookup"><span data-stu-id="062aa-115">**CreateStdAccessibleProxy**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | <span data-ttu-id="062aa-116">建立可存取的物件，這個物件具有系統提供之使用者介面專案之指定類別的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="062aa-116">Creates an accessible object that has the properties and methods of the specified class of system-provided user interface element.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="062aa-117">**LresultFromObject**</span><span class="sxs-lookup"><span data-stu-id="062aa-117">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | <span data-ttu-id="062aa-118">傳回指定之物件的參考，與控制碼類似。</span><span class="sxs-lookup"><span data-stu-id="062aa-118">Returns a reference, similar to a handle, to the specified object.</span></span> <span data-ttu-id="062aa-119">伺服器會在處理 [**WM \_ GETOBJECT**](wm-getobject.md)時傳回此參考。</span><span class="sxs-lookup"><span data-stu-id="062aa-119">Servers return this reference when handling [**WM\_GETOBJECT**](wm-getobject.md).</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="062aa-120">**ObjectFromLresult**</span><span class="sxs-lookup"><span data-stu-id="062aa-120">**ObjectFromLresult**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | <span data-ttu-id="062aa-121">根據先前產生的物件參考，抓取可存取物件的要求介面指標。</span><span class="sxs-lookup"><span data-stu-id="062aa-121">Retrieves a requested interface pointer for an accessible object based on a previously generated object reference.</span></span><br/> <span data-ttu-id="062aa-122">此函式是專為 Microsoft Active Accessibility 的內部使用所設計，而且只記載給資訊參考之用。</span><span class="sxs-lookup"><span data-stu-id="062aa-122">This function is designed for internal use by Microsoft Active Accessibility and is documented for informational purposes only.</span></span> <span data-ttu-id="062aa-123">用戶端和伺服器都不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="062aa-123">Neither clients nor servers should call this function.</span></span><br/>                               |
| [<span data-ttu-id="062aa-124">**IsWinEventHookInstalled**</span><span class="sxs-lookup"><span data-stu-id="062aa-124">**IsWinEventHookInstalled**</span></span>](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | <span data-ttu-id="062aa-125">判斷是否有已安裝的 New-winevent 勾點，可能會收到指定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="062aa-125">Determines whether there is an installed WinEvent hook that might be notified of a specified event.</span></span><br/>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="062aa-126">**NotifyWinEvent**</span><span class="sxs-lookup"><span data-stu-id="062aa-126">**NotifyWinEvent**</span></span>](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | <span data-ttu-id="062aa-127">表示發生預先定義之事件的系統。</span><span class="sxs-lookup"><span data-stu-id="062aa-127">Signals the system that a predefined event occurred.</span></span> <span data-ttu-id="062aa-128">如果有任何用戶端應用程式已為事件註冊攔截函式，系統會呼叫用戶端的攔截函式。</span><span class="sxs-lookup"><span data-stu-id="062aa-128">If any client applications have registered a hook function for the event, the system calls the client's hook function.</span></span><br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="062aa-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="062aa-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="062aa-130">Active Accessibility 消費者介面服務</span><span class="sxs-lookup"><span data-stu-id="062aa-130">Active Accessibility User Interface Services</span></span>](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 






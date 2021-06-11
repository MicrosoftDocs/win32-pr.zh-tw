---
title: '介面 (Active Accessibility 消費者介面服務) '
description: 瞭解搭配 Microsoft Active Accessibility 使用的介面，例如 IAccessible 和 IAccessibleWindowlessSite。
ms.assetid: 304ba3f8-5d1e-4a74-a0d5-36f29207f178
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8a05c55c636accba746ea79c7b13744b54d9d9
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989313"
---
# <a name="interfaces-active-accessibility-user-interface-services"></a><span data-ttu-id="0d18a-103">介面 (Active Accessibility 消費者介面服務) </span><span class="sxs-lookup"><span data-stu-id="0d18a-103">Interfaces (Active Accessibility User Interface Services)</span></span>

<span data-ttu-id="0d18a-104">本章節包含與 Microsoft Active Accessibility 搭配使用之介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0d18a-104">This section contains information about interfaces used with Microsoft Active Accessibility.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d18a-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="0d18a-105">In this section</span></span>



| <span data-ttu-id="0d18a-106">主題</span><span class="sxs-lookup"><span data-stu-id="0d18a-106">Topic</span></span>                                                                                | <span data-ttu-id="0d18a-107">描述</span><span class="sxs-lookup"><span data-stu-id="0d18a-107">Description</span></span>                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d18a-108">**IAccessible**</span><span class="sxs-lookup"><span data-stu-id="0d18a-108">**IAccessible**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)<br/>                                        | <span data-ttu-id="0d18a-109">公開方法和屬性，讓用戶端應用程式可以存取使用者介面元素及其子系。</span><span class="sxs-lookup"><span data-stu-id="0d18a-109">Exposes methods and properties that make a user interface element and its children accessible to client applications.</span></span><br/>                                                                     |
| [<span data-ttu-id="0d18a-110">**IAccessibleWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="0d18a-110">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)<br/> | <span data-ttu-id="0d18a-111">Microsoft ActiveX 控制項網站會執行這個介面，以啟用無視窗的 ActiveX 控制項，而該控制項有 Microsoft Active Accessibility 的執行來表達其存取範圍。</span><span class="sxs-lookup"><span data-stu-id="0d18a-111">A Microsoft ActiveX control site implements this interface to enable a windowless ActiveX control that has a Microsoft Active Accessibility implementation to express its accessibility.</span></span> <br/> |
| [<span data-ttu-id="0d18a-112">**IAccIdentity**</span><span class="sxs-lookup"><span data-stu-id="0d18a-112">**IAccIdentity**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity)<br/>                                      | <span data-ttu-id="0d18a-113">公開方法，這個方法會提供可存取專案的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d18a-113">Exposes a method that provides a unique identifier for an accessible element.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="0d18a-114">**IAccPropServer**</span><span class="sxs-lookup"><span data-stu-id="0d18a-114">**IAccPropServer**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)<br/>                                  | <span data-ttu-id="0d18a-115">公開方法，該方法會抓取可存取專案的屬性值。</span><span class="sxs-lookup"><span data-stu-id="0d18a-115">Exposes a method that retrieves a property value for an accessible element.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="0d18a-116">**IAccPropServices**</span><span class="sxs-lookup"><span data-stu-id="0d18a-116">**IAccPropServices**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)<br/>                              | <span data-ttu-id="0d18a-117">公開批註可存取專案和操作識別字串的方法。</span><span class="sxs-lookup"><span data-stu-id="0d18a-117">Exposes methods for annotating accessible elements and for manipulating identity strings.</span></span> <br/>                                                                                                |
| [<span data-ttu-id="0d18a-118">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="0d18a-118">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)<br/>                          | <span data-ttu-id="0d18a-119">公開方法，這個方法會從物件識別碼抓取可存取的專案。</span><span class="sxs-lookup"><span data-stu-id="0d18a-119">Exposes a method that retrieves an accessible element from an object ID.</span></span><br/>                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="0d18a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d18a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d18a-121">Active Accessibility 消費者介面服務</span><span class="sxs-lookup"><span data-stu-id="0d18a-121">Active Accessibility User Interface Services</span></span>](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 


---
title: OBJID_QUERYCLASSNAMEIDX 物件識別碼
description: Microsoft Active Accessibility 使用 OBJID \_ QUERYCLASSNAMEIDX 物件識別碼搭配 WM \_ GETOBJECT 訊息，以判斷標準 Windows 控制項或通用控制項所屬的類別。
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968011"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="5e084-103">OBJID \_ QUERYCLASSNAMEIDX 物件識別碼</span><span class="sxs-lookup"><span data-stu-id="5e084-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="5e084-104">Microsoft Active Accessibility 使用 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) 物件識別碼搭配 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，以判斷標準 Windows 控制項或通用控制項所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="5e084-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="5e084-105">控制項會藉由傳回 Microsoft Active Accessibility 對應至控制項之類別名稱的值，來回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="5e084-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="5e084-106">Microsoft Active Accessibility 使用這種資訊來提供標準 Windows 控制項和通用控制項的協助工具支援。</span><span class="sxs-lookup"><span data-stu-id="5e084-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="5e084-107">一般來說，只有標準的 Windows 控制項和通用控制項會回應 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e084-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="5e084-108">不過，如果自訂控制項包含與現有標準 Windows 控制項或通用控制項相同的所有功能，也可能會回應。</span><span class="sxs-lookup"><span data-stu-id="5e084-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="5e084-109">這可讓 Microsoft Active Accessibility 所提供的其中一個標準 proxy 物件支援自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="5e084-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="5e084-110">如需詳細資訊，請參閱 [附錄 F： OBJID \_ QUERYCLASSNAMEIDX 的物件識別碼值](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md)。</span><span class="sxs-lookup"><span data-stu-id="5e084-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 





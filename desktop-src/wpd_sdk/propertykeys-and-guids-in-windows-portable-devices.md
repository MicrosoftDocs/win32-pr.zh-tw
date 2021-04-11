---
description: Windows 可攜式裝置中的 PROPERTYKEYs 和 Guid
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: Windows 可攜式裝置中的 PROPERTYKEYs 和 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850391"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="c4d57-103">Windows 可攜式裝置中的 PROPERTYKEYs 和 Guid</span><span class="sxs-lookup"><span data-stu-id="c4d57-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="c4d57-104">屬性或命令是由 PROPERTYKEY 結構所識別。</span><span class="sxs-lookup"><span data-stu-id="c4d57-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="c4d57-105">PROPERTYKEY 結構是由兩個部分所組成： GUID (fmtid 成員) 和 (pid 成員) 的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="c4d57-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="c4d57-106">GUID 部分可用來指出屬性或命令所屬的類別 (也就是屬於相同分類的相關屬性，以及屬於相同類別的相關命令;因此，它們會有相同的 fmtid) 。</span><span class="sxs-lookup"><span data-stu-id="c4d57-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="c4d57-107">DWORD 部分表示屬性或命令識別碼，用來區別屬性或命令類別中的個別屬性或命令 (也就是說，相同類別目錄中屬性或命令的 pid 值會) 不同。</span><span class="sxs-lookup"><span data-stu-id="c4d57-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="c4d57-108">本檔的參考章節說明 WPD 定義的所有 PROPERTYKEY 值;這些值會對應至命令、屬性和資源。</span><span class="sxs-lookup"><span data-stu-id="c4d57-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="c4d57-109">如果您建立自訂 PROPERTYKEY 值，您應該定義新的 **GUID** 類別目錄。請勿重複使用 WPD **GUID** 值，或您與現有和未來 WPD 指定的 PROPERTYKEYs 有衝突的風險。</span><span class="sxs-lookup"><span data-stu-id="c4d57-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4d57-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4d57-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4d57-111">**應用程式總覽**</span><span class="sxs-lookup"><span data-stu-id="c4d57-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="c4d57-112">**命令**</span><span class="sxs-lookup"><span data-stu-id="c4d57-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="c4d57-113">**物件格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="c4d57-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="c4d57-114">**屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="c4d57-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4d57-115">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="c4d57-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 




---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: DEP/NX 相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106976630"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="99f38-103">DEP/NX 相容性</span><span class="sxs-lookup"><span data-stu-id="99f38-103">DEP/NX compatibility</span></span>

<span data-ttu-id="99f38-104">根據預設，在 Windows Internet Explorer 7 中，由於相容性的緣故，已停用 DEP/NX。</span><span class="sxs-lookup"><span data-stu-id="99f38-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="99f38-105">有幾個熱門的附加元件與 DEP/NX 不相容，而且當 Windows Internet Explorer 啟用 DEP/NX 載入時，就會失敗。</span><span class="sxs-lookup"><span data-stu-id="99f38-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="99f38-106">這些附加元件通常是使用舊版 ATL framework 所建立。</span><span class="sxs-lookup"><span data-stu-id="99f38-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="99f38-107">ATL 7.1 及更早版本不是使用 DEP 安全性功能所設計。</span><span class="sxs-lookup"><span data-stu-id="99f38-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="99f38-108">幸運的是，新版的 Microsoft Windows service pack 具有新的 DEP/NX Api，可讓您使用 DEP/NX 並保持與舊版 ATL 的相容性。</span><span class="sxs-lookup"><span data-stu-id="99f38-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="99f38-109">這些新的 Api 可讓 Internet Explorer 加入宣告 DEP/NX，而不會導致使用較舊版本的 ATL 建立的附加元件失敗。</span><span class="sxs-lookup"><span data-stu-id="99f38-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="99f38-110">當附加元件不是 DEP/NX 相容且未使用過期的 ATL 時，您可以使用群組原則選項來退出宣告 DEP/Internet Explorer NX，直到部署中斷控制項的更新版本為止。</span><span class="sxs-lookup"><span data-stu-id="99f38-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="99f38-111">本機系統管理員可以藉由以系統管理員身分執行 Internet Explorer，並在 [**網際網路選項**] 的 [ **Advanced** ] 窗格中清除 [**啟用記憶體保護**] 選項，以控制 DEP/NX。</span><span class="sxs-lookup"><span data-stu-id="99f38-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99f38-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="99f38-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99f38-113">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="99f38-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 

---
title: 安全性函數
description: 網路管理安全性功能會取得並設定以 DFS 網域為基礎和獨立根目錄的安全描述項。
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468509"
---
# <a name="security-functions"></a><span data-ttu-id="b7923-103">安全性函數</span><span class="sxs-lookup"><span data-stu-id="b7923-103">Security Functions</span></span>

<span data-ttu-id="b7923-104">網路管理安全性功能會取得並設定以 DFS 網域為基礎和獨立根目錄的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="b7923-105">DFS 安全性功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="b7923-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="b7923-106">函式</span><span class="sxs-lookup"><span data-stu-id="b7923-106">Function</span></span>                                                               | <span data-ttu-id="b7923-107">描述</span><span class="sxs-lookup"><span data-stu-id="b7923-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7923-108">**NetDfsGetSecurity**</span><span class="sxs-lookup"><span data-stu-id="b7923-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="b7923-109">取得指定之 DFS 根目錄之根物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="b7923-110">**NetDfsSetSecurity**</span><span class="sxs-lookup"><span data-stu-id="b7923-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="b7923-111">尋找指定之 DFS 根目錄的根物件，並在其上設定提供的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="b7923-112">**NetDfsGetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b7923-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="b7923-113">取得指定之 DFS 獨立根目錄之容器物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="b7923-114">**NetDfsSetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b7923-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="b7923-115">尋找指定之 DFS 獨立根目錄的容器物件，並在其上設定提供的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="b7923-116">**NetDfsGetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b7923-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="b7923-117">取得指定之 DFS 網域根目錄之容器物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="b7923-118">**NetDfsSetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b7923-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="b7923-119">尋找指定之 DFS 網域根目錄的容器物件，並在其上設定提供的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7923-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |

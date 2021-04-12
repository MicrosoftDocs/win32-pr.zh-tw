---
title: 適用于 WINPE 和伺服器 SKU 的增強式儲存體現在是選擇性的
description: 適用于 WINPE 和伺服器 SKU 的增強式儲存體現在是選擇性的
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316597"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="7b661-103">適用于 WINPE 和伺服器 SKU 的增強式儲存體現在是選擇性的</span><span class="sxs-lookup"><span data-stu-id="7b661-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="7b661-104">平台</span><span class="sxs-lookup"><span data-stu-id="7b661-104">Platforms</span></span>

<span data-ttu-id="7b661-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="7b661-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="7b661-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b661-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="7b661-107">Description</span><span class="sxs-lookup"><span data-stu-id="7b661-107">Description</span></span>

<span data-ttu-id="7b661-108">Windows 7 USB 裝置一律提供增強的儲存體。</span><span class="sxs-lookup"><span data-stu-id="7b661-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="7b661-109">在 Windows 8 版本中，它可供所有存放裝置使用。</span><span class="sxs-lookup"><span data-stu-id="7b661-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="7b661-110">在以用戶端為基礎的裝置中，預設會啟用此功能;在 [伺服器裝置] 中，它是選擇性的，必須透過 Windows 預先安裝環境 (WinPE) 布建。</span><span class="sxs-lookup"><span data-stu-id="7b661-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="7b661-111">表現</span><span class="sxs-lookup"><span data-stu-id="7b661-111">Manifestation</span></span>

<span data-ttu-id="7b661-112">如果未啟用增強型存放裝置，伺服器裝置將會失敗。</span><span class="sxs-lookup"><span data-stu-id="7b661-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="7b661-113">開機裝置必須透過已啟用的 WinPE 進行布建。</span><span class="sxs-lookup"><span data-stu-id="7b661-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="7b661-114">解決方法</span><span class="sxs-lookup"><span data-stu-id="7b661-114">Solution</span></span>

<span data-ttu-id="7b661-115">由於強化的儲存體是運行時間伺服器的選擇性選項，因此開發人員必須將其新增至 WinPE，才能布建和啟用這些磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7b661-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="7b661-116">如需詳細資訊，請參閱部署指南。</span><span class="sxs-lookup"><span data-stu-id="7b661-116">See the deployment guide for details.</span></span>

<span data-ttu-id="7b661-117">然後伺服器系統管理員必須明確設定其伺服器，以使用增強的儲存體。</span><span class="sxs-lookup"><span data-stu-id="7b661-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 





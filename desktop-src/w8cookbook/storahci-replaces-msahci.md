---
title: StorAHCI 取代 MSAHCI
description: StorAHCI 取代 MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106967292"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="f4deb-103">StorAHCI 取代 MSAHCI</span><span class="sxs-lookup"><span data-stu-id="f4deb-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="f4deb-104">平台</span><span class="sxs-lookup"><span data-stu-id="f4deb-104">Platforms</span></span>

<span data-ttu-id="f4deb-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4deb-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="f4deb-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4deb-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="f4deb-107">Description</span><span class="sxs-lookup"><span data-stu-id="f4deb-107">Description</span></span>

<span data-ttu-id="f4deb-108">StorAHCI，Storport 微型功能支援 Windows 中的序列 advanced 技術附件 (SATA) advanced host controller interface (AHCI) 控制器，並取代 MSAHCI （ATAport 的微型埠）。</span><span class="sxs-lookup"><span data-stu-id="f4deb-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f4deb-109">表現</span><span class="sxs-lookup"><span data-stu-id="f4deb-109">Manifestation</span></span>

<span data-ttu-id="f4deb-110">功能或效能都不會有任何變更;此驅動程式支援 MSAHCI 支援的所有相同裝置。</span><span class="sxs-lookup"><span data-stu-id="f4deb-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="f4deb-111">這項變更對使用者而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="f4deb-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f4deb-112">降低</span><span class="sxs-lookup"><span data-stu-id="f4deb-112">Mitigation</span></span>

<span data-ttu-id="f4deb-113">更新依賴 ATAport 系結的任何公用程式和腳本。</span><span class="sxs-lookup"><span data-stu-id="f4deb-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="f4deb-114">請勿依賴磁片磁碟機名稱。</span><span class="sxs-lookup"><span data-stu-id="f4deb-114">Do not rely on the drive name.</span></span> <span data-ttu-id="f4deb-115">改為使用標準磁片偵測。</span><span class="sxs-lookup"><span data-stu-id="f4deb-115">Instead use standard disk detection.</span></span>

 

 





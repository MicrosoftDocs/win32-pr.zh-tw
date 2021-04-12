---
title: NDIS 6.30 驅動程式的埠3已淘汰
description: NDIS 6.30 驅動程式的埠3已淘汰
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463833"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="9791b-103">NDIS 6.30 驅動程式的埠3已淘汰</span><span class="sxs-lookup"><span data-stu-id="9791b-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="9791b-104">平台</span><span class="sxs-lookup"><span data-stu-id="9791b-104">Platforms</span></span>

<span data-ttu-id="9791b-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="9791b-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="9791b-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9791b-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="9791b-107">Description</span><span class="sxs-lookup"><span data-stu-id="9791b-107">Description</span></span>

<span data-ttu-id="9791b-108">Windows 8 移除適用于 NDIS 微型埠 WLAN 驅動程式的平臺支援，以建立或啟動 IHV 擴充性埠 (也稱為第三個埠) 。</span><span class="sxs-lookup"><span data-stu-id="9791b-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="9791b-109">這項功能是在 Windows 7 中引進作為暫時量值，而 Wi-Fi 聯盟 (WFA) 開發 Wi-Fi 直接規格。</span><span class="sxs-lookup"><span data-stu-id="9791b-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="9791b-110">規格現在已完成，使用 Wi-Fi Direct 的產品已通過認證，Windows 8 引進原生 Wi-Fi 直接堆疊。</span><span class="sxs-lookup"><span data-stu-id="9791b-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9791b-111">表現</span><span class="sxs-lookup"><span data-stu-id="9791b-111">Manifestation</span></span>

<span data-ttu-id="9791b-112">沒有，因為第三個埠是 WLAN 微型埠驅動程式需要這項功能時，會啟動的平臺功能。</span><span class="sxs-lookup"><span data-stu-id="9791b-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="9791b-113">解決方法</span><span class="sxs-lookup"><span data-stu-id="9791b-113">Solution</span></span>

<span data-ttu-id="9791b-114">我們會將擴充性埠功能保留給未回報 NDIS 6.30 的現有驅動程式，以維持裝置相容性。</span><span class="sxs-lookup"><span data-stu-id="9791b-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="9791b-115">不過，報告 NDIS 6.30 的新 WLAN 驅動程式將無法啟動此埠;相反地，這些驅動程式的開發人員應該使用 Wi-Fi Direct。</span><span class="sxs-lookup"><span data-stu-id="9791b-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 





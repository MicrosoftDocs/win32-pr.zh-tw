---
description: 色板是一個陣列，其中包含的色彩值會識別目前可在輸出裝置上顯示或繪製的色彩。
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: " (Windows GDI) 的調色板"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114696"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="046ec-103"> (Windows GDI) 的調色板</span><span class="sxs-lookup"><span data-stu-id="046ec-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="046ec-104">色板是一個陣列，其中包含的色彩值會識別目前可在輸出裝置上顯示或繪製的色彩。</span><span class="sxs-lookup"><span data-stu-id="046ec-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="046ec-105">色彩調色板是由能夠產生許多色彩的裝置所使用，但在任何指定時間只能顯示或繪製這些色彩的子集。</span><span class="sxs-lookup"><span data-stu-id="046ec-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="046ec-106">針對這類裝置，系統會維護 *系統元件* ，以追蹤和管理裝置目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="046ec-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="046ec-107">應用程式無法直接存取系統調色板。</span><span class="sxs-lookup"><span data-stu-id="046ec-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="046ec-108">相反地，系統會將預設的調色板與每個裝置內容產生關聯。</span><span class="sxs-lookup"><span data-stu-id="046ec-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="046ec-109">應用程式可以使用預設調色板中的色彩，或藉由建立 *邏輯調色板* 並將它們與個別裝置內容產生關聯，來定義自己的色彩。</span><span class="sxs-lookup"><span data-stu-id="046ec-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="046ec-110">應用程式可以 \_ 在 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式所傳回的 RASTERCAPS 值中檢查 RC 選擇區位，藉以判斷裝置是否支援色彩調色板。</span><span class="sxs-lookup"><span data-stu-id="046ec-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 




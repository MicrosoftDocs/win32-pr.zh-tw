---
description: 針對可延伸位旗標資料常數，服務提供者廠商可以定義指定位的新值。
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag 資料常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989317"
---
# <a name="bit-flag-data-constants"></a><span data-ttu-id="e8dc2-103">Bit-Flag 資料常數</span><span class="sxs-lookup"><span data-stu-id="e8dc2-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="e8dc2-104">針對可延伸位旗標資料常數，服務提供者廠商可以定義指定位的新值。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="e8dc2-105">因為大部分位旗標常數都是 **DWORD**，所以較低位的特定數目通常會保留給一般擴充，而其餘的位則適用于廠商專屬的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="e8dc2-106">一般位旗標是從位零開始指派，而廠商專屬的延伸模組則應從位31下指派。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="e8dc2-107">此配置提供最大的彈性，可將位位置指派給通用擴充功能，而不是廠商專屬的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="e8dc2-108">廠商預期會定義新的值，這些值是 API 所定義之位旗標的自然延伸。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="e8dc2-109">可擴充的資料結構具有大小可變大小的欄位，保留給裝置特定用途。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="e8dc2-110">因為欄位是大小可變大小，所以服務提供者會決定欄位的資訊和轉譯量。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="e8dc2-111">定義裝置特定欄位的廠商預期會讓 API 所定義的原始資料結構自然擴充。</span><span class="sxs-lookup"><span data-stu-id="e8dc2-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 




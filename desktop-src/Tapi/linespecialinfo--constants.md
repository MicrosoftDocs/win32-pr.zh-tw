---
description: LINESPECIALINFO \_ 位旗標常數描述網路可用來報告各種報告和網路觀察作業的特殊資訊信號。
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: 'LINESPECIALINFO_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989559"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="d57f4-103">LINESPECIALINFO \_ 常數</span><span class="sxs-lookup"><span data-stu-id="d57f4-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="d57f4-104">**LINESPECIALINFO \_** 位旗標常數描述網路可用來報告各種報告和網路觀察作業的特殊資訊信號。</span><span class="sxs-lookup"><span data-stu-id="d57f4-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="d57f4-105">它們是在網路諮詢記錄的公告開頭傳送的特殊編碼語氣序列。</span><span class="sxs-lookup"><span data-stu-id="d57f4-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="d57f4-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**</span><span class="sxs-lookup"><span data-stu-id="d57f4-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d57f4-107">這項特殊資訊語氣優先于空白號碼、AIS、Centrex 數位變更和非工作站、存取程式碼未撥打或撥入錯誤，或手動攔截操作員訊息 (客戶 irregularity 類別) 。</span><span class="sxs-lookup"><span data-stu-id="d57f4-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="d57f4-108">\_當帳單資訊遭到拒絕，以及在切換時封鎖撥號位址時，也會回報 LINESPECIALINFO CUSTIRREG。</span><span class="sxs-lookup"><span data-stu-id="d57f4-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d57f4-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOCIRCUIT**</span><span class="sxs-lookup"><span data-stu-id="d57f4-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d57f4-110">這種特殊資訊語氣會在沒有線路或緊急公告之前 (主幹封鎖類別) 。</span><span class="sxs-lookup"><span data-stu-id="d57f4-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d57f4-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO \_ 重新排序**</span><span class="sxs-lookup"><span data-stu-id="d57f4-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d57f4-112">這種特殊資訊語氣優先于重新訂購公告 (設備 irregularity 類別) 。</span><span class="sxs-lookup"><span data-stu-id="d57f4-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="d57f4-113">\_當電話保持 offhook 太長時，也會回報 LINESPECIALINFO 重新排序。</span><span class="sxs-lookup"><span data-stu-id="d57f4-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d57f4-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="d57f4-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d57f4-115">有關特殊資訊語氣的詳細資料無法使用，也不會變成已知。</span><span class="sxs-lookup"><span data-stu-id="d57f4-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d57f4-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="d57f4-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d57f4-117">有關特殊資訊語氣的詳細資訊目前不明，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="d57f4-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d57f4-118">備註</span><span class="sxs-lookup"><span data-stu-id="d57f4-118">Remarks</span></span>

<span data-ttu-id="d57f4-119">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="d57f4-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="d57f4-120">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="d57f4-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="d57f4-121">系統會針對諮詢訊息定義特殊的資訊色調，而且通常不會用於計費或監督用途。</span><span class="sxs-lookup"><span data-stu-id="d57f4-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57f4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d57f4-122">Requirements</span></span>



| <span data-ttu-id="d57f4-123">需求</span><span class="sxs-lookup"><span data-stu-id="d57f4-123">Requirement</span></span> | <span data-ttu-id="d57f4-124">值</span><span class="sxs-lookup"><span data-stu-id="d57f4-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d57f4-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d57f4-125">TAPI version</span></span><br/> | <span data-ttu-id="d57f4-126">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d57f4-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d57f4-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d57f4-127">Header</span></span><br/>       | <dl> <span data-ttu-id="d57f4-128"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="d57f4-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 





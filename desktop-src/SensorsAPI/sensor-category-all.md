---
description: '[感應器 \_ 類別] 類別 \_ 代表所有平臺定義的感應器類別的集合。'
ms.assetid: e2d9fe6d-450a-446b-968b-0924116af6fe
title: 'SENSOR_CATEGORY_ALL (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2e5641e51dde130cc51d9b2fc35fcc1e158ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690087"
---
# <a name="sensor_category_all"></a><span data-ttu-id="5186a-103">感應器 \_ 類別目錄 \_</span><span class="sxs-lookup"><span data-stu-id="5186a-103">SENSOR\_CATEGORY\_ALL</span></span>

<span data-ttu-id="5186a-104">[感應器 \_ 類別] 類別 \_ 代表所有平臺定義的感應器類別的集合。</span><span class="sxs-lookup"><span data-stu-id="5186a-104">The SENSOR\_CATEGORY\_ALL category represents the set of all platform-defined sensor categories.</span></span>

<span data-ttu-id="5186a-105">**平臺定義的屬性索引鍵**</span><span class="sxs-lookup"><span data-stu-id="5186a-105">**Platform-Defined Property Keys**</span></span>

<span data-ttu-id="5186a-106">此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 一般 \_ GUID 為基礎：</span><span class="sxs-lookup"><span data-stu-id="5186a-106">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_COMMON\_GUID:</span></span>

<span data-ttu-id="5186a-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span><span class="sxs-lookup"><span data-stu-id="5186a-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span></span>

<span data-ttu-id="5186a-108">下表描述平臺定義的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="5186a-108">The following table describes platform-defined data fields.</span></span>



| <span data-ttu-id="5186a-109">資料欄位名稱和 PID</span><span class="sxs-lookup"><span data-stu-id="5186a-109">Data field name and PID</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="5186a-110">Description</span><span class="sxs-lookup"><span data-stu-id="5186a-110">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_TIMESTAMP"></span><span id="sensor_data_type_timestamp"></span><dl> <span data-ttu-id="5186a-111"><dt>**感應器 \_資料 \_ 類型 \_ 時間戳記**</dt> <dt> (PID = 2 )</dt></span><span class="sxs-lookup"><span data-stu-id="5186a-111"><dt>**SENSOR\_DATA\_TYPE\_TIMESTAMP**</dt> <dt>(PID = 2 ) </dt></span></span> </dl> | <span data-ttu-id="5186a-112">**VT \_ FILETIME**</span><span class="sxs-lookup"><span data-stu-id="5186a-112">**VT\_FILETIME**</span></span><br/> <span data-ttu-id="5186a-113">所有資料包表都需要。</span><span class="sxs-lookup"><span data-stu-id="5186a-113">Required for all data reports.</span></span> <span data-ttu-id="5186a-114">以國際標準時間 (UTC) 格式，將每個資料包表標記為資料包表的建立時間。</span><span class="sxs-lookup"><span data-stu-id="5186a-114">Marks each data report with the time the data report was created in Coordinated Universal Time (UTC) format.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5186a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5186a-115">Requirements</span></span>



| <span data-ttu-id="5186a-116">需求</span><span class="sxs-lookup"><span data-stu-id="5186a-116">Requirement</span></span> | <span data-ttu-id="5186a-117">值</span><span class="sxs-lookup"><span data-stu-id="5186a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5186a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5186a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5186a-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5186a-119">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5186a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5186a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5186a-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="5186a-121">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5186a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5186a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5186a-123"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="5186a-123"><dt>Sensors.h</dt></span></span> </dl> |



 

 





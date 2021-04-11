---
description: 感應器 \_ 類別 \_ 掃描器類別包含的感應器，可提供掃描所取得的資訊。
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: 'SENSOR_CATEGORY_SCANNER (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943316"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="57903-103">感應器 \_ 類別 \_ 掃描器</span><span class="sxs-lookup"><span data-stu-id="57903-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="57903-104">感應器 \_ 類別 \_ 掃描器類別包含的感應器，可提供掃描所取得的資訊。</span><span class="sxs-lookup"><span data-stu-id="57903-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="57903-105">**平臺定義的感應器類型**</span><span class="sxs-lookup"><span data-stu-id="57903-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="57903-106">此類別包括下列平臺定義的感應器類型。</span><span class="sxs-lookup"><span data-stu-id="57903-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="57903-107">感應器類型</span><span class="sxs-lookup"><span data-stu-id="57903-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="57903-108">Description</span><span class="sxs-lookup"><span data-stu-id="57903-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="57903-109"><dt>**感應器 \_輸入 \_ 條碼 \_ 掃描器**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span><span class="sxs-lookup"><span data-stu-id="57903-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="57903-110">使用光學掃描來讀取條碼的感應器。</span><span class="sxs-lookup"><span data-stu-id="57903-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="57903-111"><dt>**感應器 \_輸入 \_ RFID \_ 掃描器**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span><span class="sxs-lookup"><span data-stu-id="57903-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="57903-112">無線電頻率識別碼掃描感應器。</span><span class="sxs-lookup"><span data-stu-id="57903-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="57903-113">**平臺定義的資料欄位**</span><span class="sxs-lookup"><span data-stu-id="57903-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="57903-114">此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 掃描器 \_ GUID 為基礎：</span><span class="sxs-lookup"><span data-stu-id="57903-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="57903-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="57903-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="57903-116">此類別包括下列的平臺定義資料欄位。</span><span class="sxs-lookup"><span data-stu-id="57903-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="57903-117">資料欄位名稱和 PID</span><span class="sxs-lookup"><span data-stu-id="57903-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="57903-118">Description</span><span class="sxs-lookup"><span data-stu-id="57903-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="57903-119"><dt>**感應器 \_資料 \_ 類型 \_ RFID \_ 標記 \_ 40 \_ 位**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="57903-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="57903-120">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="57903-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="57903-121">40位的電臺頻率識別碼標記值。</span><span class="sxs-lookup"><span data-stu-id="57903-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="57903-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="57903-122">Requirements</span></span>



| <span data-ttu-id="57903-123">需求</span><span class="sxs-lookup"><span data-stu-id="57903-123">Requirement</span></span> | <span data-ttu-id="57903-124">值</span><span class="sxs-lookup"><span data-stu-id="57903-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57903-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57903-125">Minimum supported client</span></span><br/> | <span data-ttu-id="57903-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57903-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57903-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57903-127">Minimum supported server</span></span><br/> | <span data-ttu-id="57903-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="57903-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="57903-129">標頭</span><span class="sxs-lookup"><span data-stu-id="57903-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="57903-130"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="57903-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 





---
description: Windows 映像取得 (WIA) 2.0 專案會分組為類別，以定義如何處理或使用 IWiaItem2。
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: 'WIA 2.0 專案類別目錄 Guid (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966722"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="c9004-103">WIA 2.0 專案類別目錄 Guid</span><span class="sxs-lookup"><span data-stu-id="c9004-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="c9004-104">Windows 映像取得 (WIA) 2.0 專案會分組為類別，以定義如何處理或使用 [**IWiaItem2**](-wia-iwiaitem2.md) 。</span><span class="sxs-lookup"><span data-stu-id="c9004-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="c9004-105">例如，如果專案代表送紙器，則應用程式應該會預期它包含所需的檔送紙器屬性，並如同檔輸送器般運作。</span><span class="sxs-lookup"><span data-stu-id="c9004-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="c9004-106">如果專案代表已完成的檔案，則 WIA 2.0 應用程式應該以這種方式處理，並假設資料是靜態的，而且位於裝置上。</span><span class="sxs-lookup"><span data-stu-id="c9004-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="c9004-107"> (每個專案的規則都會在其個別規格檔中定義。 ) 每個類別都有 GUID 類型常數。</span><span class="sxs-lookup"><span data-stu-id="c9004-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="c9004-108">常數</span><span class="sxs-lookup"><span data-stu-id="c9004-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="c9004-109">描述</span><span class="sxs-lookup"><span data-stu-id="c9004-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="c9004-110"><dt>**WIA \_ 類別 \_ AUTO**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="c9004-111">代表支援自動設定掃描之 WIA 2.0 掃描器裝置自動設定設定的專案。</span><span class="sxs-lookup"><span data-stu-id="c9004-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="c9004-112"><dt>**WIA \_ 類別 \_ 送紙器**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="c9004-113">這是可程式化資料來源的送紙器專案，並遵循支援檔送紙器所需的標準規則和屬性集。</span><span class="sxs-lookup"><span data-stu-id="c9004-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="c9004-114"><dt>**WIA \_ 類別 \_ 送 \_ 回送回**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="c9004-115">描述雙工基底送紙器專案的後端資料來源的可程式化資料來源。</span><span class="sxs-lookup"><span data-stu-id="c9004-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="c9004-116"><dt>**WIA \_ 類別 \_ 送紙器 \_ 正面**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="c9004-117">描述雙工基底送紙器專案之前端資料來源的可程式化資料來源。</span><span class="sxs-lookup"><span data-stu-id="c9004-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="c9004-118"><dt>**WIA \_ 類別 \_ 膠捲**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="c9004-119">這是可程式化資料來源的電影專案，並遵循支援膠捲掃描單位所需的標準規則和屬性集。</span><span class="sxs-lookup"><span data-stu-id="c9004-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="c9004-120"><dt>**WIA \_ 類別 \_ 已完成檔案 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="c9004-121">不是可程式化資料來源的專案，或以完成檔案格式提供資料的專案，或包含已完成檔案格式專案的資料夾專案。</span><span class="sxs-lookup"><span data-stu-id="c9004-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="c9004-122"><dt>**WIA \_ 類別的 \_ 平板**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="c9004-123">平板專案，它是可程式化的資料來源，並遵循支援平板影印掃描所需的標準規則和屬性集。</span><span class="sxs-lookup"><span data-stu-id="c9004-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="c9004-124"><dt>**WIA \_ 類別 \_ 目錄資料夾**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="c9004-125">資料夾儲存專案 (不是可程式化的資料來源，) 包含其他資料夾專案或完成的檔案或兩者。</span><span class="sxs-lookup"><span data-stu-id="c9004-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="c9004-126"><dt>**WIA \_ 類別 \_ 根目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="c9004-127">裝置的根專案。</span><span class="sxs-lookup"><span data-stu-id="c9004-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="c9004-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9004-128">Requirements</span></span>



| <span data-ttu-id="c9004-129">需求</span><span class="sxs-lookup"><span data-stu-id="c9004-129">Requirement</span></span> | <span data-ttu-id="c9004-130">值</span><span class="sxs-lookup"><span data-stu-id="c9004-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9004-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9004-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c9004-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9004-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c9004-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9004-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c9004-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9004-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9004-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c9004-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9004-136"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9004-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 





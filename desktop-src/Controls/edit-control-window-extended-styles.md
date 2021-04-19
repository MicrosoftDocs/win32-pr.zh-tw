---
title: '編輯控制項擴充樣式 (CommCtrl .h) '
description: 本節列出建立編輯控制項時使用的擴充樣式。 擴充樣式的值是這些樣式的位元組合。
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993311"
---
# <a name="edit-control-extended-styles"></a><span data-ttu-id="8f2f7-104">編輯控制項延伸樣式</span><span class="sxs-lookup"><span data-stu-id="8f2f7-104">Edit Control Extended Styles</span></span>

<span data-ttu-id="8f2f7-105">本節列出建立編輯控制項時使用的擴充樣式。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-105">This section lists extended styles used when creating edit controls.</span></span> <span data-ttu-id="8f2f7-106">擴充樣式的值是這些樣式的位元組合。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-106">The value of extended styles is a bitwise combination of these styles.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8f2f7-107">常數</span><span class="sxs-lookup"><span data-stu-id="8f2f7-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8f2f7-108">描述</span><span class="sxs-lookup"><span data-stu-id="8f2f7-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <span data-ttu-id="8f2f7-109"><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f2f7-109"><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8f2f7-110">[Windows Vista](common-control-versions.md)（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-110">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="8f2f7-111">啟用支援換行字元 (CR) 行尾字元。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-111">Enables support for carriage return (CR) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <span data-ttu-id="8f2f7-112"><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f2f7-112"><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8f2f7-113">[Windows Vista](common-control-versions.md)（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-113">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="8f2f7-114">可支援換行字元 (LF) 行尾字元，以分隔行。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-114">Enables support for linefeed (LF) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <span data-ttu-id="8f2f7-115"><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f2f7-115"><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8f2f7-116">[Windows Vista](common-control-versions.md)（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-116">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="8f2f7-117">可支援換行字元 (CR) 和換行字元 (LF) 行尾字元，以分隔行。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-117">Enables support for both carriage return (CR) and linefeed (LF) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <span data-ttu-id="8f2f7-118"><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f2f7-118"><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8f2f7-119">[Windows Vista](common-control-versions.md)（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-119">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="8f2f7-120">轉換貼上內容中此編輯控制項的已啟用行尾字元，以符合目前檔所使用的行尾字元。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-120">Converts end-of-line characters enabled for this edit control in pasted content to match the end-of-line character used by the current document.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <span data-ttu-id="8f2f7-121"><dt><strong>ES_EX_ZOOMABLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8f2f7-121"><dt><strong>ES_EX_ZOOMABLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8f2f7-122">[Windows Vista](common-control-versions.md)（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-122">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="8f2f7-123">使用 Ctrl + 滑鼠滾輪和 [**em \_ GETZOOM**](em-getzoom.md) / [**em \_ SETZOOM**](em-setzoom.md)訊息來啟用縮放。</span><span class="sxs-lookup"><span data-stu-id="8f2f7-123">Enables zooming using Ctrl+MouseWheel and the [**EM\_GETZOOM**](em-getzoom.md)/[**EM\_SETZOOM**](em-setzoom.md) messages.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="8f2f7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f2f7-124">Requirements</span></span>



| <span data-ttu-id="8f2f7-125">需求</span><span class="sxs-lookup"><span data-stu-id="8f2f7-125">Requirement</span></span> | <span data-ttu-id="8f2f7-126">值</span><span class="sxs-lookup"><span data-stu-id="8f2f7-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2f7-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8f2f7-127">Header</span></span><br/> | <dl> <span data-ttu-id="8f2f7-128"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2f7-128"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






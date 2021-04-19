---
description: TUISPIDLL \_ 物件定義如下。
ms.assetid: bc0f876d-2443-4c3c-b723-3f82dc6bf849
title: 'TUISPIDLL_OBJECT_ (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a4711478b98f1ab4983fd8c83a59772e5b370e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998892"
---
# <a name="tuispidll_object_"></a><span data-ttu-id="b5aec-103">TUISPIDLL \_ 物件\_</span><span class="sxs-lookup"><span data-stu-id="b5aec-103">TUISPIDLL\_OBJECT\_</span></span>

<dl> <dt>

<span data-ttu-id="b5aec-104"><span id="TUISPIDLL_OBJECT_LINEID"></span><span id="tuispidll_object_lineid"></span>**TUISPIDLL \_ 物件 \_ LINEID**</span><span class="sxs-lookup"><span data-stu-id="b5aec-104"><span id="TUISPIDLL_OBJECT_LINEID"></span><span id="tuispidll_object_lineid"></span>**TUISPIDLL\_OBJECT\_LINEID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b5aec-105">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b5aec-105">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="b5aec-106">*dwObjectID* 是行裝置識別碼， (dwDeviceID) 。</span><span class="sxs-lookup"><span data-stu-id="b5aec-106">*dwObjectID* is a line device identifier (dwDeviceID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b5aec-107"><span id="TUISPIDLL_OBJECT_PHONEID"></span><span id="tuispidll_object_phoneid"></span>**TUISPIDLL \_ 物件 \_ PHONEID**</span><span class="sxs-lookup"><span data-stu-id="b5aec-107"><span id="TUISPIDLL_OBJECT_PHONEID"></span><span id="tuispidll_object_phoneid"></span>**TUISPIDLL\_OBJECT\_PHONEID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b5aec-108">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b5aec-108">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="b5aec-109">*dwObjectID* 是電話裝置識別碼 (dwDeviceID) 。</span><span class="sxs-lookup"><span data-stu-id="b5aec-109">*dwObjectID* is a phone device identifier (dwDeviceID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b5aec-110"><span id="TUISPIDLL_OBJECT_PROVIDERID"></span><span id="tuispidll_object_providerid"></span>**TUISPIDLL \_ 物件 \_ PROVIDERID**</span><span class="sxs-lookup"><span data-stu-id="b5aec-110"><span id="TUISPIDLL_OBJECT_PROVIDERID"></span><span id="tuispidll_object_providerid"></span>**TUISPIDLL\_OBJECT\_PROVIDERID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b5aec-111">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b5aec-111">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="b5aec-112">*dwObjectID* 是永久性的提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5aec-112">*dwObjectID* is a permanent provider identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b5aec-113"><span id="TUISPIDLL_OBJECT_DIALOGINSTANCE"></span><span id="tuispidll_object_dialoginstance"></span>**TUISPIDLL \_ 物件 \_ DIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="b5aec-113"><span id="TUISPIDLL_OBJECT_DIALOGINSTANCE"></span><span id="tuispidll_object_dialoginstance"></span>**TUISPIDLL\_OBJECT\_DIALOGINSTANCE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b5aec-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b5aec-114">0x00000004</span></span> 
</dt> <dt>



<span data-ttu-id="b5aec-115">*dwObjectID* 是根據內容) ， (HDRVDIALOGINSTANCE 或 HTAPIDIALOGINSTANCE 的對話方塊實例。</span><span class="sxs-lookup"><span data-stu-id="b5aec-115">*dwObjectID* is a dialog instance handle (either HDRVDIALOGINSTANCE or HTAPIDIALOGINSTANCE, depending on the context).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5aec-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5aec-116">Requirements</span></span>



| <span data-ttu-id="b5aec-117">需求</span><span class="sxs-lookup"><span data-stu-id="b5aec-117">Requirement</span></span> | <span data-ttu-id="b5aec-118">值</span><span class="sxs-lookup"><span data-stu-id="b5aec-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b5aec-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b5aec-119">TAPI version</span></span><br/> | <span data-ttu-id="b5aec-120">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b5aec-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b5aec-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b5aec-121">Header</span></span><br/>       | <dl> <span data-ttu-id="b5aec-122"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5aec-122"><dt>Tspi.h</dt></span></span> </dl> |



 

 





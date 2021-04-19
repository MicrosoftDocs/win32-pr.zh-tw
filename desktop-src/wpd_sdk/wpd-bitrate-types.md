---
description: WPD \_ 位元速率 \_ 類型列舉類型會描述音訊檔案壓縮類型。
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: 'WPD_BITRATE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993534"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="0aca7-103">WPD \_ 位元速率 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="0aca7-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="0aca7-104">**WPD \_ 位元速率 \_ 類型** 列舉類型會描述音訊檔案的壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="0aca7-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aca7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0aca7-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="0aca7-106">常數</span><span class="sxs-lookup"><span data-stu-id="0aca7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0aca7-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_未使用 WPD 位元速率 \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="0aca7-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="0aca7-108">未指定這個值。</span><span class="sxs-lookup"><span data-stu-id="0aca7-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="0aca7-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD \_ 位元速率 \_ 類型 \_ 離散**</span><span class="sxs-lookup"><span data-stu-id="0aca7-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="0aca7-110">固定位元速率壓縮。</span><span class="sxs-lookup"><span data-stu-id="0aca7-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="0aca7-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD \_ 位元速率 \_ 類型 \_ 變數**</span><span class="sxs-lookup"><span data-stu-id="0aca7-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0aca7-112">變數位元速率壓縮。</span><span class="sxs-lookup"><span data-stu-id="0aca7-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="0aca7-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD \_ 位元速率 \_ 類型 \_ 免費**</span><span class="sxs-lookup"><span data-stu-id="0aca7-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="0aca7-114">自由格式位速度。</span><span class="sxs-lookup"><span data-stu-id="0aca7-114">Free format bit rate.</span></span> <span data-ttu-id="0aca7-115">這是比允許的最大位元速率低的固定位元速率。</span><span class="sxs-lookup"><span data-stu-id="0aca7-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0aca7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aca7-116">Requirements</span></span>



| <span data-ttu-id="0aca7-117">需求</span><span class="sxs-lookup"><span data-stu-id="0aca7-117">Requirement</span></span> | <span data-ttu-id="0aca7-118">值</span><span class="sxs-lookup"><span data-stu-id="0aca7-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aca7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0aca7-119">Header</span></span><br/> | <dl> <span data-ttu-id="0aca7-120"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="0aca7-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aca7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aca7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aca7-122">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="0aca7-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 





---
description: WPD \_ 焦點 \_ 模式列舉類型會說明靜止影像捕獲裝置所使用的焦點模式。
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: 'WPD_FOCUS_MODES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994740"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="dd0b9-103">WPD \_ 焦點 \_ 模式列舉</span><span class="sxs-lookup"><span data-stu-id="dd0b9-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="dd0b9-104">**WPD \_ 焦點 \_ 模式** 列舉類型會說明靜止影像捕獲裝置所使用的焦點模式。</span><span class="sxs-lookup"><span data-stu-id="dd0b9-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd0b9-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="dd0b9-106">常數</span><span class="sxs-lookup"><span data-stu-id="dd0b9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd0b9-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**\_ \_ 未定義 WPD 焦點**</span><span class="sxs-lookup"><span data-stu-id="dd0b9-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="dd0b9-108">尚未指定焦點模式。</span><span class="sxs-lookup"><span data-stu-id="dd0b9-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="dd0b9-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD \_ 焦點 \_ 手冊**</span><span class="sxs-lookup"><span data-stu-id="dd0b9-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="dd0b9-110">指定手動焦點。</span><span class="sxs-lookup"><span data-stu-id="dd0b9-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="dd0b9-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_自動 WPD 焦點 \_**</span><span class="sxs-lookup"><span data-stu-id="dd0b9-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="dd0b9-112">指定由裝置控制的自動焦點。</span><span class="sxs-lookup"><span data-stu-id="dd0b9-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="dd0b9-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD \_ 焦點 \_ 自動 \_ 宏**</span><span class="sxs-lookup"><span data-stu-id="dd0b9-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="dd0b9-114">指定裝置應該視需要自動切換宏和一般焦點。</span><span class="sxs-lookup"><span data-stu-id="dd0b9-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd0b9-115">備註</span><span class="sxs-lookup"><span data-stu-id="dd0b9-115">Remarks</span></span>

<span data-ttu-id="dd0b9-116">[WPD \_ 仍 \_ 影像 \_ 焦點 \_ 模式](still-image-properties.md)屬性會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="dd0b9-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0b9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd0b9-117">Requirements</span></span>



| <span data-ttu-id="dd0b9-118">需求</span><span class="sxs-lookup"><span data-stu-id="dd0b9-118">Requirement</span></span> | <span data-ttu-id="dd0b9-119">值</span><span class="sxs-lookup"><span data-stu-id="dd0b9-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0b9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dd0b9-120">Header</span></span><br/> | <dl> <span data-ttu-id="dd0b9-121"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0b9-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0b9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd0b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0b9-123">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="dd0b9-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 





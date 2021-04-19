---
description: 描述單一色彩值的結構。
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: 'XPS_COLOR (Xpsobjectmodel) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975460"
---
# <a name="xps_color"></a><span data-ttu-id="df94a-103">XPS \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="df94a-103">XPS\_COLOR</span></span>

<span data-ttu-id="df94a-104">描述單一色彩值的結構。</span><span class="sxs-lookup"><span data-stu-id="df94a-104">A structure that describes a single color value.</span></span>

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a><span data-ttu-id="df94a-105">備註</span><span class="sxs-lookup"><span data-stu-id="df94a-105">Remarks</span></span>

<span data-ttu-id="df94a-106">結構的格式取決於 *colorType* 的值。</span><span class="sxs-lookup"><span data-stu-id="df94a-106">The structure's format depends on the value of *colorType*.</span></span>

<dl>

<span data-ttu-id="df94a-107">[**XPS \_ 色彩 \_ 類型 \_ SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df94a-107">[**XPS\_COLOR\_TYPE\_SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span></span>  
<span data-ttu-id="df94a-108">[**XPS \_ 色彩 \_ 類型 \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df94a-108">[**XPS\_COLOR\_TYPE\_SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span></span>  
[<span data-ttu-id="df94a-109">**XPS \_ 色彩 \_ 類型 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="df94a-109">**XPS\_COLOR\_TYPE\_CONTEXT**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a><span data-ttu-id="df94a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="df94a-110">Requirements</span></span>



| <span data-ttu-id="df94a-111">需求</span><span class="sxs-lookup"><span data-stu-id="df94a-111">Requirement</span></span> | <span data-ttu-id="df94a-112">值</span><span class="sxs-lookup"><span data-stu-id="df94a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df94a-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df94a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="df94a-114">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="df94a-114">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="df94a-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df94a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="df94a-116">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df94a-116">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="df94a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="df94a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="df94a-118"><dt>Xpsobjectmodel。h</dt></span><span class="sxs-lookup"><span data-stu-id="df94a-118"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                              |
| <span data-ttu-id="df94a-119">Idl</span><span class="sxs-lookup"><span data-stu-id="df94a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df94a-120"><dt>XpsObjectModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="df94a-120"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                            |



## <a name="see-also"></a><span data-ttu-id="df94a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df94a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df94a-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="df94a-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 


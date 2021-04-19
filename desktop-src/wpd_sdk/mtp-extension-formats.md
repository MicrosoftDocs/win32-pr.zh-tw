---
description: MTP 延伸格式
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: MTP 延伸格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985666"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="78c00-103">MTP 延伸格式</span><span class="sxs-lookup"><span data-stu-id="78c00-103">MTP Extension Formats</span></span>

<span data-ttu-id="78c00-104">裝置上的檔案格式可由 GUID 值描述。</span><span class="sxs-lookup"><span data-stu-id="78c00-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="78c00-105">這個值是由 [WPD \_ 物件格式] 屬性所指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="78c00-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="78c00-106">廠商延伸格式</span><span class="sxs-lookup"><span data-stu-id="78c00-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="78c00-107">當裝置製造商支援廠商延伸格式時，其驅動程式會將廠商的格式代碼 (UINT16) 與 **WPD \_ 物件 \_ 格式 \_ 未指定** GUID 的最高16位結合在一起。</span><span class="sxs-lookup"><span data-stu-id="78c00-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="78c00-108">例如，如果廠商擴充的程式碼是0xB001，則產生的 GUID 會如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="78c00-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="78c00-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="78c00-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78c00-110">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="78c00-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




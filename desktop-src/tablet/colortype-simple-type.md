---
description: 定義型別，這個型別是用來針對日誌 XML 檔案中特定專案的色彩指定有效值。
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: ColorType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966661"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="5c1ad-103">ColorType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="5c1ad-103">ColorType Simple Type</span></span>

<span data-ttu-id="5c1ad-104">定義型別，這個型別是用來針對日誌 XML 檔案中特定專案的色彩指定有效值。</span><span class="sxs-lookup"><span data-stu-id="5c1ad-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="5c1ad-105">備註</span><span class="sxs-lookup"><span data-stu-id="5c1ad-105">Remarks</span></span>

<span data-ttu-id="5c1ad-106">色彩可以是 RRGGBB 格式的十六進位 RGB 值 \# 。</span><span class="sxs-lookup"><span data-stu-id="5c1ad-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="5c1ad-107">它必須符合下列正則運算式： \# \[ 0-9A-FA-F \] {6} 。</span><span class="sxs-lookup"><span data-stu-id="5c1ad-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="5c1ad-108">例如： " \# 4a79B5"。</span><span class="sxs-lookup"><span data-stu-id="5c1ad-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1ad-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c1ad-109">Requirements</span></span>



| <span data-ttu-id="5c1ad-110">需求</span><span class="sxs-lookup"><span data-stu-id="5c1ad-110">Requirement</span></span> | <span data-ttu-id="5c1ad-111">值</span><span class="sxs-lookup"><span data-stu-id="5c1ad-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5c1ad-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c1ad-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5c1ad-113">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c1ad-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5c1ad-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c1ad-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5c1ad-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="5c1ad-115">None supported</span></span><br/>                                     |



 

 





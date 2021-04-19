---
description: View 類別中的每個屬性都必須有一個稱為 PropertySources 的字串陣列限定詞。
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: PropertySources 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979031"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="77087-103">PropertySources 辨識符號</span><span class="sxs-lookup"><span data-stu-id="77087-103">PropertySources Qualifier</span></span>

<span data-ttu-id="77087-104">View 類別中的每個屬性都必須有一個稱為 **PropertySources** 的字串陣列限定詞。</span><span class="sxs-lookup"><span data-stu-id="77087-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="77087-105">**PropertySources** 辨識符號包含來源類別屬性的名稱，或此 view 類別屬性從中取得資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="77087-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="77087-106">這個陣列中的值順序會對應到針對 [ViewSources 限定詞](viewsources-qualifier.md)定義之來源類別的順序。</span><span class="sxs-lookup"><span data-stu-id="77087-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="77087-107">下列範例將示範如何定義 union view 類別的屬性，這是來自兩部不同電腦的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別聯集：</span><span class="sxs-lookup"><span data-stu-id="77087-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="77087-108">第一個 **DeviceID** 屬性會對應到第一個來源查詢中類別的 **deviceid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="77087-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="77087-109">第二個 **DeviceID** 屬性是第二個來源查詢中類別的 **deviceid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="77087-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="77087-110">定義聯結視圖類別的屬性時，您必須為每個來源類別屬性定義個別的 view 屬性，除非來源類別屬性是聯結視圖類別的基礎。</span><span class="sxs-lookup"><span data-stu-id="77087-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="77087-111">下列範例會在與 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer) 來源類別和 [**win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) 來源類別相似的屬性上，于聯結視圖類別中建立屬性：</span><span class="sxs-lookup"><span data-stu-id="77087-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="77087-112">如果兩個來源類別是由通用屬性聯結，您只能定義單一 view 類別屬性，因為這兩個來源類別屬性的值一律相同。</span><span class="sxs-lookup"><span data-stu-id="77087-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="77087-113">下列範例示範如何透過通用屬性值加入 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer) 類別和 [**win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) ：</span><span class="sxs-lookup"><span data-stu-id="77087-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="77087-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="77087-114">Requirements</span></span>



| <span data-ttu-id="77087-115">需求</span><span class="sxs-lookup"><span data-stu-id="77087-115">Requirement</span></span> | <span data-ttu-id="77087-116">值</span><span class="sxs-lookup"><span data-stu-id="77087-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="77087-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77087-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77087-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77087-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="77087-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77087-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77087-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77087-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77087-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77087-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77087-122">**視圖提供者專用的限定詞**</span><span class="sxs-lookup"><span data-stu-id="77087-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 


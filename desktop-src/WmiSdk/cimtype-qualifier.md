---
description: CIMType 限定詞包含描述屬性類型的文字。
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: CIMType 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115868"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="a24f9-103">CIMType 辨識符號</span><span class="sxs-lookup"><span data-stu-id="a24f9-103">CIMType Qualifier</span></span>

<span data-ttu-id="a24f9-104">**CIMType** 限定詞包含描述屬性類型的文字。</span><span class="sxs-lookup"><span data-stu-id="a24f9-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="a24f9-105">此文字可以是 MOF 類型，例如 "string" 和 "sint32"，或 CIM 類型，例如 "CIM \_ string" 和 "cim \_ sint32"。</span><span class="sxs-lookup"><span data-stu-id="a24f9-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="a24f9-106">**CIMType** 限定詞與 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)方法的 *pvtType* 參數中所使用的屬性類型之間有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="a24f9-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="a24f9-107">這兩個例外狀況如下：</span><span class="sxs-lookup"><span data-stu-id="a24f9-107">The two exceptions are:</span></span>

-   <span data-ttu-id="a24f9-108">[*參考屬性*](gloss-r.md)，其類型為 **CIM \_ 參考**，其中包含 "REF： classname" 值。</span><span class="sxs-lookup"><span data-stu-id="a24f9-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="a24f9-109">Classname 值描述參考屬性的類別類型。</span><span class="sxs-lookup"><span data-stu-id="a24f9-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="a24f9-110">具有 **CIM \_ 物件** 類型的内嵌物件屬性。</span><span class="sxs-lookup"><span data-stu-id="a24f9-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="a24f9-111">不過請注意， **CIMType** 限定詞可以和應該用來更精確地輸入參考屬性。</span><span class="sxs-lookup"><span data-stu-id="a24f9-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="a24f9-112">例如，如果屬性永遠參考 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的實例，其 **CIMType** 限定詞應設定為：</span><span class="sxs-lookup"><span data-stu-id="a24f9-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="a24f9-113">根據預設，參考屬性的 **CIMType** 限定詞具有類型 **ref**。</span><span class="sxs-lookup"><span data-stu-id="a24f9-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="a24f9-114">如同參考屬性， **CIMType** 限定詞應該用來以下列語法更精確地輸入内嵌物件屬性：</span><span class="sxs-lookup"><span data-stu-id="a24f9-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="a24f9-115">由於 WMI 允許的類型比使用 VT 前置詞的標準常數來表示的類型多 \_ ， **CIMType** 限定詞可協助解讀型別值。</span><span class="sxs-lookup"><span data-stu-id="a24f9-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="a24f9-116">系統會自動新增 **CIMType** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="a24f9-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="a24f9-117">如需詳細資訊，請參閱 [MOF 資料類型](mof-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a24f9-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a24f9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a24f9-118">Requirements</span></span>



| <span data-ttu-id="a24f9-119">需求</span><span class="sxs-lookup"><span data-stu-id="a24f9-119">Requirement</span></span> | <span data-ttu-id="a24f9-120">值</span><span class="sxs-lookup"><span data-stu-id="a24f9-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a24f9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a24f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a24f9-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a24f9-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a24f9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a24f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a24f9-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a24f9-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a24f9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a24f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24f9-126">**標準 WMI 限定詞**</span><span class="sxs-lookup"><span data-stu-id="a24f9-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="a24f9-127">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="a24f9-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="a24f9-128">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="a24f9-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 


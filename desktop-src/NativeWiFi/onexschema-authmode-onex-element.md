---
description: 指定用於驗證的認證類型。
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: authMode (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991861"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="0fb2f-103">authMode (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="0fb2f-103">authMode (OneX) Element</span></span>

<span data-ttu-id="0fb2f-104">AuthMode (OneX) 元素會指定用於驗證的認證類型。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="0fb2f-105">下表說明可能出現的值。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="0fb2f-106">值</span><span class="sxs-lookup"><span data-stu-id="0fb2f-106">Value</span></span>         | <span data-ttu-id="0fb2f-107">描述</span><span class="sxs-lookup"><span data-stu-id="0fb2f-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb2f-108">machineOrUser</span><span class="sxs-lookup"><span data-stu-id="0fb2f-108">machineOrUser</span></span> | <span data-ttu-id="0fb2f-109">使用電腦或使用者認證。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-109">Use machine or user credentials.</span></span> <span data-ttu-id="0fb2f-110">當使用者登入時，會使用使用者的認證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="0fb2f-111">當使用者未登入時，會使用電腦認證。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="0fb2f-112">機器</span><span class="sxs-lookup"><span data-stu-id="0fb2f-112">machine</span></span>       | <span data-ttu-id="0fb2f-113">只使用電腦認證。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="0fb2f-114">使用者</span><span class="sxs-lookup"><span data-stu-id="0fb2f-114">user</span></span>          | <span data-ttu-id="0fb2f-115">僅使用使用者認證。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="0fb2f-116">guest</span><span class="sxs-lookup"><span data-stu-id="0fb2f-116">guest</span></span>         | <span data-ttu-id="0fb2f-117">僅使用來賓 (空白) 認證。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="0fb2f-118">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-118">This element is optional.</span></span> <span data-ttu-id="0fb2f-119">當設定檔中未指定 authMode 時， `machineOrUser` 會使用的值。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="0fb2f-120">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0fb2f-121">**AuthMode** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fb2f-122">備註</span><span class="sxs-lookup"><span data-stu-id="0fb2f-122">Remarks</span></span>

<span data-ttu-id="0fb2f-123">您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="0fb2f-124">如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="0fb2f-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb2f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fb2f-125">Requirements</span></span>



| <span data-ttu-id="0fb2f-126">需求</span><span class="sxs-lookup"><span data-stu-id="0fb2f-126">Requirement</span></span> | <span data-ttu-id="0fb2f-127">值</span><span class="sxs-lookup"><span data-stu-id="0fb2f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fb2f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fb2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb2f-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fb2f-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0fb2f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fb2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb2f-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fb2f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fb2f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fb2f-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fb2f-133">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="0fb2f-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0fb2f-134">**OneX**</span><span class="sxs-lookup"><span data-stu-id="0fb2f-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="0fb2f-135">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="0fb2f-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0fb2f-136">**OneX**</span><span class="sxs-lookup"><span data-stu-id="0fb2f-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 

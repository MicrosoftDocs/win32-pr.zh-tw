---
title: IWMDRMLicense 介面
description: IWMDRMLicense 介面代表一或多個授權的清單。
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- IWMDRMLicense 介面 windows 媒體格式
- IWMDRMLicense 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463376"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="83903-105">IWMDRMLicense 介面</span><span class="sxs-lookup"><span data-stu-id="83903-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="83903-106">**IWMDRMLicense** 介面代表一或多個授權的清單。</span><span class="sxs-lookup"><span data-stu-id="83903-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="83903-107">成員</span><span class="sxs-lookup"><span data-stu-id="83903-107">Members</span></span>

<span data-ttu-id="83903-108">**IWMDRMLicense** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="83903-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="83903-109">**IWMDRMLicense** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83903-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="83903-110">方法</span><span class="sxs-lookup"><span data-stu-id="83903-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="83903-111">方法</span><span class="sxs-lookup"><span data-stu-id="83903-111">Methods</span></span>

<span data-ttu-id="83903-112">**IWMDRMLicense** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="83903-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="83903-113">方法</span><span class="sxs-lookup"><span data-stu-id="83903-113">Method</span></span>                                                                                   | <span data-ttu-id="83903-114">描述</span><span class="sxs-lookup"><span data-stu-id="83903-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83903-115">**CanPersist**</span><span class="sxs-lookup"><span data-stu-id="83903-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="83903-116">查詢授權是否可保存在本機授權存放區中。</span><span class="sxs-lookup"><span data-stu-id="83903-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="83903-117">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="83903-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="83903-118">使用目前授權的設定建立解密程式物件。</span><span class="sxs-lookup"><span data-stu-id="83903-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="83903-119">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="83903-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="83903-120">使用目前授權的設定建立加密程式物件。</span><span class="sxs-lookup"><span data-stu-id="83903-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="83903-121">**CreateSecureDecryptor**</span><span class="sxs-lookup"><span data-stu-id="83903-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="83903-122">建立安全的解密子物件。</span><span class="sxs-lookup"><span data-stu-id="83903-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="83903-123">安全解密程式與一般解密程式不同，因為它會解密內容，然後根據此方法的參數中指定的設定重新加密。</span><span class="sxs-lookup"><span data-stu-id="83903-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="83903-124">**GetAnalogVideoRestrictionLevels**</span><span class="sxs-lookup"><span data-stu-id="83903-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="83903-125">抓取目前授權所設定的所有類比影片限制。</span><span class="sxs-lookup"><span data-stu-id="83903-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="83903-126">**GetInclusionList**</span><span class="sxs-lookup"><span data-stu-id="83903-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="83903-127">抓取目前授權或授權鏈的整個包含清單。</span><span class="sxs-lookup"><span data-stu-id="83903-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="83903-128">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="83903-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="83903-129">以可延伸標記語言 (XML)  (XML) 或可延伸媒體許可權 (XMR) 資料的形式抓取授權。</span><span class="sxs-lookup"><span data-stu-id="83903-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="83903-130">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="83903-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="83903-131">從目前的授權抓取屬性。</span><span class="sxs-lookup"><span data-stu-id="83903-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="83903-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="83903-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="83903-133">載入清單中下一個授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83903-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="83903-134">**GetOutputProtectionLevels**</span><span class="sxs-lookup"><span data-stu-id="83903-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="83903-135">抓取指派給授權 (OPLs) 之所有輸出保護層級的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83903-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="83903-136">**PersistLicense**</span><span class="sxs-lookup"><span data-stu-id="83903-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="83903-137">將目前的授權從暫時存放區儲存到永久本機授權存放區。</span><span class="sxs-lookup"><span data-stu-id="83903-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="83903-138">**ResetEnumeration**</span><span class="sxs-lookup"><span data-stu-id="83903-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="83903-139">將授權清單重設為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="83903-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="83903-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83903-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83903-141">**介面**</span><span class="sxs-lookup"><span data-stu-id="83903-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 


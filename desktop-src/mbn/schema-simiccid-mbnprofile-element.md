---
description: 識別 GSM 裝置的 SIM 識別碼。
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: SimIccID (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970804"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="ebbc1-103">SimIccID (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="ebbc1-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="ebbc1-104">**SimIccID (MBNProfile)** 元素會識別適用于 GSM 裝置的 SIM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebbc1-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="ebbc1-105">這個元素是選擇性的，且由行動寬頻服務設定供內部使用。</span><span class="sxs-lookup"><span data-stu-id="ebbc1-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="ebbc1-106">應用程式在建立或更新設定檔時，不應設定此欄位。</span><span class="sxs-lookup"><span data-stu-id="ebbc1-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="ebbc1-107">**SimIccID** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="ebbc1-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbc1-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebbc1-108">Requirements</span></span>



| <span data-ttu-id="ebbc1-109">需求</span><span class="sxs-lookup"><span data-stu-id="ebbc1-109">Requirement</span></span> | <span data-ttu-id="ebbc1-110">值</span><span class="sxs-lookup"><span data-stu-id="ebbc1-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ebbc1-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebbc1-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbc1-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebbc1-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ebbc1-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebbc1-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbc1-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="ebbc1-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ebbc1-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebbc1-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebbc1-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="ebbc1-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ebbc1-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="ebbc1-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="ebbc1-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="ebbc1-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ebbc1-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="ebbc1-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 





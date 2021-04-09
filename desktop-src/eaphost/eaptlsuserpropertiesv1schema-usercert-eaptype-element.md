---
title: UserCert (EapType) 元素
description: 指應用於驗證的憑證 SHA-1 雜湊。
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- UserCert 元素 EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686332"
---
# <a name="usercert-eaptype-element"></a><span data-ttu-id="a2dce-104">UserCert (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="a2dce-104">UserCert (EapType) Element</span></span>

<span data-ttu-id="a2dce-105">**UserCert (EapType)** 元素指的是應用於驗證的憑證 sha-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="a2dce-105">The **UserCert (EapType)** element refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span>

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

<span data-ttu-id="a2dce-106">**UserCert** 元素是由 [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="a2dce-106">The **UserCert** element is defined by the [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2dce-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2dce-107">Requirements</span></span>



| <span data-ttu-id="a2dce-108">需求</span><span class="sxs-lookup"><span data-stu-id="a2dce-108">Requirement</span></span> | <span data-ttu-id="a2dce-109">值</span><span class="sxs-lookup"><span data-stu-id="a2dce-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2dce-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2dce-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a2dce-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2dce-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a2dce-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2dce-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a2dce-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2dce-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2dce-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2dce-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2dce-115">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="a2dce-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a2dce-116">**EapType**</span><span class="sxs-lookup"><span data-stu-id="a2dce-116">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="a2dce-117">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="a2dce-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a2dce-118">**EapType**</span><span class="sxs-lookup"><span data-stu-id="a2dce-118">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="a2dce-119">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="a2dce-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a2dce-120">eaptlsuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="a2dce-120">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






---
description: 指定行動電話網路的相關資訊。
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: " (行動寬頻) 的 providerType 複雜類型"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972648"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="f02f5-103">providerType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="f02f5-103">providerType Complex Type</span></span>

<span data-ttu-id="f02f5-104">**ProviderType** 複雜類型會指定行動電話通訊網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f02f5-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f02f5-105">子元素</span><span class="sxs-lookup"><span data-stu-id="f02f5-105">Child elements</span></span>



| <span data-ttu-id="f02f5-106">元素</span><span class="sxs-lookup"><span data-stu-id="f02f5-106">Element</span></span>                                                          | <span data-ttu-id="f02f5-107">類型</span><span class="sxs-lookup"><span data-stu-id="f02f5-107">Type</span></span>                                                           | <span data-ttu-id="f02f5-108">Description</span><span class="sxs-lookup"><span data-stu-id="f02f5-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="f02f5-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="f02f5-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="f02f5-110">**providerIdType**</span><span class="sxs-lookup"><span data-stu-id="f02f5-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="f02f5-111">提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f02f5-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="f02f5-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f02f5-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="f02f5-113">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="f02f5-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="f02f5-114">提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="f02f5-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f02f5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f02f5-115">Requirements</span></span>



| <span data-ttu-id="f02f5-116">需求</span><span class="sxs-lookup"><span data-stu-id="f02f5-116">Requirement</span></span> | <span data-ttu-id="f02f5-117">值</span><span class="sxs-lookup"><span data-stu-id="f02f5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f02f5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f02f5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f02f5-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f02f5-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f02f5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f02f5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f02f5-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="f02f5-121">None supported</span></span><br/>                         |



 

 





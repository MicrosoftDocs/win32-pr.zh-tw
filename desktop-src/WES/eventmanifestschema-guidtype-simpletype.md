---
title: 'GUIDType 簡單類型 (EventManifest 架構) '
description: '以登錄格式定義全域唯一識別碼型別。 |GUIDType 簡單類型 (EventManifest 架構) '
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- GUIDType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986070"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a><span data-ttu-id="4e064-105">GUIDType 簡單類型 (EventManifest 架構) </span><span class="sxs-lookup"><span data-stu-id="4e064-105">GUIDType Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="4e064-106">以登錄格式定義全域唯一識別碼型別。</span><span class="sxs-lookup"><span data-stu-id="4e064-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="4e064-107">模式</span><span class="sxs-lookup"><span data-stu-id="4e064-107">Patterns</span></span>

<span data-ttu-id="4e064-108">**GUIDType** 簡單類型是以下列模式限制的字串：</span><span class="sxs-lookup"><span data-stu-id="4e064-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="4e064-109">此值必須是登錄格式的全域唯一識別碼類型。</span><span class="sxs-lookup"><span data-stu-id="4e064-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="4e064-110">例如，{5b2fc63a-8af4-44cb-960c-aefdced908d6}。</span><span class="sxs-lookup"><span data-stu-id="4e064-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="4e064-111">使用 GUIDGen.exe 或 UUIDGen.exe 建立 GUID。</span><span class="sxs-lookup"><span data-stu-id="4e064-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e064-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e064-112">Requirements</span></span>



| <span data-ttu-id="4e064-113">需求</span><span class="sxs-lookup"><span data-stu-id="4e064-113">Requirement</span></span> | <span data-ttu-id="4e064-114">值</span><span class="sxs-lookup"><span data-stu-id="4e064-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e064-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e064-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4e064-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e064-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4e064-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e064-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4e064-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e064-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






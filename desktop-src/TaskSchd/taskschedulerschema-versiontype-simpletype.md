---
title: versionType 簡單類型
description: 定義指定工作版本的模式。
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- versionType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317171"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="1f182-104">versionType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="1f182-104">versionType Simple Type</span></span>

<span data-ttu-id="1f182-105">定義指定工作版本的模式。</span><span class="sxs-lookup"><span data-stu-id="1f182-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="1f182-106">模式</span><span class="sxs-lookup"><span data-stu-id="1f182-106">Patterns</span></span>

<span data-ttu-id="1f182-107">**VersionType** 簡單類型是以下列模式限制的 **字串**：</span><span class="sxs-lookup"><span data-stu-id="1f182-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="1f182-108">後面接著一、二或三個雙精度浮點數的雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="1f182-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="1f182-109">例如，1.2 或1.2.3。</span><span class="sxs-lookup"><span data-stu-id="1f182-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f182-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f182-110">Requirements</span></span>



| <span data-ttu-id="1f182-111">需求</span><span class="sxs-lookup"><span data-stu-id="1f182-111">Requirement</span></span> | <span data-ttu-id="1f182-112">值</span><span class="sxs-lookup"><span data-stu-id="1f182-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f182-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f182-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1f182-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f182-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f182-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f182-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1f182-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f182-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






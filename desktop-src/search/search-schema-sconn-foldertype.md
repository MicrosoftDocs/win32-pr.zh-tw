---
description: <folderType>元素指定資料夾類型的 GUID。 如果元素存在，則需要這個元素 <templateInfo> 。 它沒有屬性和子項目。
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: 'folderType 元素 (搜尋連接器架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468788"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="eb11d-105">folderType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="eb11d-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="eb11d-106"><folderType>元素指定資料夾類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="eb11d-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="eb11d-107">如果元素存在，則需要這個元素 <templateInfo> 。</span><span class="sxs-lookup"><span data-stu-id="eb11d-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="eb11d-108">它沒有屬性和子項目。</span><span class="sxs-lookup"><span data-stu-id="eb11d-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb11d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb11d-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="eb11d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="eb11d-110">Element Information</span></span>



| <span data-ttu-id="eb11d-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="eb11d-111">Parent Element</span></span>                                                                         | <span data-ttu-id="eb11d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="eb11d-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="eb11d-113">templateInfo 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="eb11d-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="eb11d-114">備註</span><span class="sxs-lookup"><span data-stu-id="eb11d-114">Remarks</span></span>

<span data-ttu-id="eb11d-115">預設 GUID 是 {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}，這是同盟搜尋 (OpenSearch) 連接器的一般資料夾類型。</span><span class="sxs-lookup"><span data-stu-id="eb11d-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="eb11d-116">FolderType 元素範例</span><span class="sxs-lookup"><span data-stu-id="eb11d-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 




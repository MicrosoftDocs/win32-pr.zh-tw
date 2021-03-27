---
description: <folderType>元素指定資料夾類型的 GUID。 如果專案存在，則需要這個元素 <templateInfo> ，否則它是選擇性的。 此元素沒有屬性和子項目。
title: 'folderType 元素 (程式庫架構) '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972301"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="1f833-105">folderType 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="1f833-106"><folderType>元素指定資料夾類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1f833-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="1f833-107">如果專案存在，則需要這個元素 <templateInfo> ，否則它是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1f833-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="1f833-108">此元素沒有屬性和子項目。</span><span class="sxs-lookup"><span data-stu-id="1f833-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f833-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f833-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1f833-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1f833-110">Element Information</span></span>



| <span data-ttu-id="1f833-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="1f833-111">Parent Element</span></span>                                                           | <span data-ttu-id="1f833-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1f833-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="1f833-113">templateInfo 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="1f833-114">備註</span><span class="sxs-lookup"><span data-stu-id="1f833-114">Remarks</span></span>

<span data-ttu-id="1f833-115">設定資料夾類型會決定預設會出現在 Windows 檔案總管中的資料行和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1f833-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="1f833-116">資料夾類型識別碼 ([**FOLDERTYPEID**](foldertypeid.md)) 是在 Shlguid 中定義的 guid。</span><span class="sxs-lookup"><span data-stu-id="1f833-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="1f833-117">下表列出一般資料夾類型的 Guid。</span><span class="sxs-lookup"><span data-stu-id="1f833-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="1f833-118">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="1f833-118">Folder Type</span></span>      | <span data-ttu-id="1f833-119">GUID</span><span class="sxs-lookup"><span data-stu-id="1f833-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="1f833-120">一般程式庫</span><span class="sxs-lookup"><span data-stu-id="1f833-120">Generic Library</span></span>  | <span data-ttu-id="1f833-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="1f833-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="1f833-122">使用者程式庫</span><span class="sxs-lookup"><span data-stu-id="1f833-122">Users Libraries</span></span>  | <span data-ttu-id="1f833-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="1f833-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="1f833-124">檔資料夾</span><span class="sxs-lookup"><span data-stu-id="1f833-124">Documents Folder</span></span> | <span data-ttu-id="1f833-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span><span class="sxs-lookup"><span data-stu-id="1f833-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="1f833-126">圖片資料夾</span><span class="sxs-lookup"><span data-stu-id="1f833-126">Pictures Folder</span></span>  | <span data-ttu-id="1f833-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="1f833-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="1f833-128">影片資料夾</span><span class="sxs-lookup"><span data-stu-id="1f833-128">Videos Folder</span></span>    | <span data-ttu-id="1f833-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="1f833-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="1f833-130">遊戲資料夾</span><span class="sxs-lookup"><span data-stu-id="1f833-130">Games Folder</span></span>     | <span data-ttu-id="1f833-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="1f833-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="1f833-132">音樂資料夾</span><span class="sxs-lookup"><span data-stu-id="1f833-132">Music Folder</span></span>     | <span data-ttu-id="1f833-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span><span class="sxs-lookup"><span data-stu-id="1f833-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="1f833-134">連絡人</span><span class="sxs-lookup"><span data-stu-id="1f833-134">Contacts</span></span>         | <span data-ttu-id="1f833-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="1f833-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1f833-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f833-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f833-137">iconReference 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="1f833-138">isLibraryPinned 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="1f833-139">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="1f833-140"> (程式庫架構的 name 元素) </span><span class="sxs-lookup"><span data-stu-id="1f833-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="1f833-141">ownerSID 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="1f833-142">propertyStore 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="1f833-143">searchConnectorDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="1f833-144">searchConnectorDescriptionList 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="1f833-145">templateInfo 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="1f833-146">version 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="1f833-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 




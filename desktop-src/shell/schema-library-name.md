---
description: <name>元素指定此程式庫的名稱。 此為必要專案，而且沒有任何屬性或子項目。
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: " (程式庫架構的 name 元素) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991811"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="60471-104"> (程式庫架構的 name 元素) </span><span class="sxs-lookup"><span data-stu-id="60471-104">name Element (Library Schema)</span></span>

<span data-ttu-id="60471-105"><name>元素指定此程式庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="60471-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="60471-106">此為必要專案，而且沒有任何屬性或子項目。</span><span class="sxs-lookup"><span data-stu-id="60471-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="60471-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60471-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="60471-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="60471-108">Element Information</span></span>



| <span data-ttu-id="60471-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="60471-109">Parent Element</span></span>                                                               | <span data-ttu-id="60471-110">子元素</span><span class="sxs-lookup"><span data-stu-id="60471-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="60471-111">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="60471-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="60471-112">備註</span><span class="sxs-lookup"><span data-stu-id="60471-112">Remarks</span></span>

<span data-ttu-id="60471-113">名稱是顯示在 Windows 檔案總管中的易記程式庫名稱。</span><span class="sxs-lookup"><span data-stu-id="60471-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="60471-114">您可以使用格式來指定名稱 <dllname> ， <index> 如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="60471-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="60471-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="60471-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60471-116">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="60471-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="60471-117">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="60471-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 

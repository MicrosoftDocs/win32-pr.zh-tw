---
description: 定義型別，該型別定義 Content 專案日誌讀取器之 Type 屬性的有效值 \[ \] 。
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: ContentTypeType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026902"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="38caa-103">ContentTypeType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="38caa-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="38caa-104">定義型別，該型別定義 [Content 專案 \[ 日誌讀取 \] 器](content-element--journal-reader.md)之 *type* 屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="38caa-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="38caa-105">模式</span><span class="sxs-lookup"><span data-stu-id="38caa-105">Patterns</span></span>

<span data-ttu-id="38caa-106">**ContentTypeType** 簡單類型是以下列模式限制的字串：</span><span class="sxs-lookup"><span data-stu-id="38caa-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="38caa-107">備註</span><span class="sxs-lookup"><span data-stu-id="38caa-107">Remarks</span></span>

<span data-ttu-id="38caa-108">有效的值為 "Normal" 和 "惰性"。</span><span class="sxs-lookup"><span data-stu-id="38caa-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="38caa-109">如果類型是 "惰性"，則包含的內容會是記錄頁面，它是檔的唯讀/不可編輯的「背景」。</span><span class="sxs-lookup"><span data-stu-id="38caa-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="38caa-110">使用筆記本便箋寫入器印表機驅動程式建立檔時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="38caa-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="38caa-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="38caa-111">Requirements</span></span>



| <span data-ttu-id="38caa-112">需求</span><span class="sxs-lookup"><span data-stu-id="38caa-112">Requirement</span></span> | <span data-ttu-id="38caa-113">值</span><span class="sxs-lookup"><span data-stu-id="38caa-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="38caa-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38caa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="38caa-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38caa-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="38caa-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38caa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="38caa-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="38caa-117">None supported</span></span><br/>                                     |



 

 





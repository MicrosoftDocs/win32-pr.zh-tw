---
title: 'CSymbolType 簡單類型 (Windows 事件記錄檔) '
description: CSymbolType Simple Type (Windows 事件記錄檔) -定義有效的 C/c + + 符號名稱。
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- CSymbolType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090616"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="ffbda-104">CSymbolType 簡單類型 (Windows 事件記錄檔) </span><span class="sxs-lookup"><span data-stu-id="ffbda-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="ffbda-105">定義有效的 C/c + + 符號名稱。</span><span class="sxs-lookup"><span data-stu-id="ffbda-105">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="ffbda-106">模式</span><span class="sxs-lookup"><span data-stu-id="ffbda-106">Patterns</span></span>

<span data-ttu-id="ffbda-107">**CSymbolType** 簡單類型是以下列模式限制的 **xs： string** ：</span><span class="sxs-lookup"><span data-stu-id="ffbda-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="ffbda-108">符號名稱可以是空的，或包含英數位元和底線。</span><span class="sxs-lookup"><span data-stu-id="ffbda-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="ffbda-109">如果名稱是空的，訊息編譯器將會產生符號名稱。</span><span class="sxs-lookup"><span data-stu-id="ffbda-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="ffbda-110">如果您指定名稱，則名稱必須以底線 (開頭 \_) 或字母字元。</span><span class="sxs-lookup"><span data-stu-id="ffbda-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffbda-111">備註</span><span class="sxs-lookup"><span data-stu-id="ffbda-111">Remarks</span></span>

<span data-ttu-id="ffbda-112">如果符號名稱是空的，訊息編譯器會使用您定義之專案的 **name** 屬性來產生符號名稱。</span><span class="sxs-lookup"><span data-stu-id="ffbda-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="ffbda-113">編譯器會以底線取代任何非英數位元和前置數位。</span><span class="sxs-lookup"><span data-stu-id="ffbda-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="ffbda-114">例如，如果通道的 **名稱** 屬性是 Microsoft-Windows-SampleProvider/Operational，編譯器會使用 Microsoft \_ Windows \_ SampleProvider 作業 \_ 做為符號名稱。</span><span class="sxs-lookup"><span data-stu-id="ffbda-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbda-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffbda-115">Requirements</span></span>



| <span data-ttu-id="ffbda-116">需求</span><span class="sxs-lookup"><span data-stu-id="ffbda-116">Requirement</span></span> | <span data-ttu-id="ffbda-117">值</span><span class="sxs-lookup"><span data-stu-id="ffbda-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ffbda-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffbda-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbda-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffbda-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ffbda-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffbda-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbda-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffbda-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






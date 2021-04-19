---
description: '深入瞭解： JET_SESID。ToString 方法 (字串，IFormatProvider) '
title: 'JET_SESID。ToString 方法 (字串，IFormatProvider) '
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512468
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5565e67cc0f91fd1c2edb0d9c0aa421211c57c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972009"
---
# <a name="jet_sesidtostring-method-string-iformatprovider"></a><span data-ttu-id="f51c0-103">JET_SESID。ToString 方法 (字串，IFormatProvider) </span><span class="sxs-lookup"><span data-stu-id="f51c0-103">JET_SESID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="f51c0-104">使用指定的格式，格式化目前執行個體的值。</span><span class="sxs-lookup"><span data-stu-id="f51c0-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="f51c0-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f51c0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f51c0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f51c0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f51c0-107">語法</span><span class="sxs-lookup"><span data-stu-id="f51c0-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_SESID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="f51c0-108">參數</span><span class="sxs-lookup"><span data-stu-id="f51c0-108">Parameters</span></span>

  - <span data-ttu-id="f51c0-109">format</span><span class="sxs-lookup"><span data-stu-id="f51c0-109">format</span></span>  
    <span data-ttu-id="f51c0-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f51c0-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f51c0-111">[字串](/dotnet/api/system.string)，指定要使用的格式;或者，null 會使用針對[>iformattable](/dotnet/api/system.iformattable)實作為型別所定義的預設格式。</span><span class="sxs-lookup"><span data-stu-id="f51c0-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="f51c0-112">>formatprovider</span><span class="sxs-lookup"><span data-stu-id="f51c0-112">formatProvider</span></span>  
    <span data-ttu-id="f51c0-113">類型： [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="f51c0-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="f51c0-114">要用來格式化值的 [IFormatProvider](/dotnet/api/system.iformatprovider) ;或者，若要從作業系統的目前地區設定取得數值格式資訊，則為 null。</span><span class="sxs-lookup"><span data-stu-id="f51c0-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f51c0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f51c0-115">Return value</span></span>

<span data-ttu-id="f51c0-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f51c0-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="f51c0-117">[字串](/dotnet/api/system.string)，包含指定格式之目前實例的值。</span><span class="sxs-lookup"><span data-stu-id="f51c0-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="f51c0-118">實作</span><span class="sxs-lookup"><span data-stu-id="f51c0-118">Implements</span></span>

[<span data-ttu-id="f51c0-119">>iformattable (字串，IFormatProvider) </span><span class="sxs-lookup"><span data-stu-id="f51c0-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="f51c0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f51c0-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f51c0-121">參考</span><span class="sxs-lookup"><span data-stu-id="f51c0-121">Reference</span></span>

[<span data-ttu-id="f51c0-122">JET_SESID 結構</span><span class="sxs-lookup"><span data-stu-id="f51c0-122">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="f51c0-123">JET_SESID 成員</span><span class="sxs-lookup"><span data-stu-id="f51c0-123">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="f51c0-124">ToString 多載</span><span class="sxs-lookup"><span data-stu-id="f51c0-124">ToString overload</span></span>](./jet-sesid.tostring-method2.md)

[<span data-ttu-id="f51c0-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f51c0-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

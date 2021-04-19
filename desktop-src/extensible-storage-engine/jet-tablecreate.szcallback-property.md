---
description: 深入瞭解： JET_TABLECREATE szCallback 屬性
title: JET_TABLECREATE szCallback 屬性
TOCTitle: 'szCallback property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.szcallback(v=EXCHG.10)
ms:contentKeyID: 55103969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a987f274cf82ebdc3c2113fd1636174c51382f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973604"
---
# <a name="jet_tablecreateszcallback-property"></a><span data-ttu-id="14870-103">JET_TABLECREATE szCallback 屬性</span><span class="sxs-lookup"><span data-stu-id="14870-103">JET_TABLECREATE.szCallback property</span></span>

<span data-ttu-id="14870-104">取得或設定要用於資料表的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="14870-104">Gets or sets a callback function to use for the table.</span></span> <span data-ttu-id="14870-105">這是 "module \! functionName" 形式，並假設非受控碼。</span><span class="sxs-lookup"><span data-stu-id="14870-105">This is in the form "module\!functionName", and assumes unmanaged code.</span></span> <span data-ttu-id="14870-106">如需替代方法，請參閱 **JetRegisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp、JET_CALLBACK、IntPtr、JET_HANDLE)** 。</span><span class="sxs-lookup"><span data-stu-id="14870-106">See **JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)** for an alternative.</span></span>

<span data-ttu-id="14870-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14870-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14870-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="14870-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14870-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="14870-109">Syntax</span></span>

``` vb
'Declaration
Public Property szCallback As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szCallback

instance.szCallback = value
```

``` csharp
public string szCallback { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="14870-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="14870-110">Property value</span></span>

<span data-ttu-id="14870-111">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="14870-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="14870-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14870-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14870-113">參考</span><span class="sxs-lookup"><span data-stu-id="14870-113">Reference</span></span>

[<span data-ttu-id="14870-114">JET_TABLECREATE 類別</span><span class="sxs-lookup"><span data-stu-id="14870-114">JET_TABLECREATE class</span></span>](./jet-tablecreate-class.md)

[<span data-ttu-id="14870-115">JET_TABLECREATE 成員</span><span class="sxs-lookup"><span data-stu-id="14870-115">JET_TABLECREATE members</span></span>](./jet-tablecreate-members.md)

[<span data-ttu-id="14870-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="14870-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

---
title: TreatAs
description: 指定可模擬目前類別之類別的 CLSID。
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- TreatAs 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840283"
---
# <a name="treatas"></a><span data-ttu-id="3a950-104">TreatAs</span><span class="sxs-lookup"><span data-stu-id="3a950-104">TreatAs</span></span>

<span data-ttu-id="3a950-105">指定可模擬目前類別之類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="3a950-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3a950-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="3a950-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="3a950-107">備註</span><span class="sxs-lookup"><span data-stu-id="3a950-107">Remarks</span></span>

<span data-ttu-id="3a950-108">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="3a950-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="3a950-109">模擬可以讓某個應用程式開啟和編輯不同類別的物件，同時保留物件的原始格式。</span><span class="sxs-lookup"><span data-stu-id="3a950-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="3a950-110">解析發生在本機電腦上，因此在遠端啟動案例中，解析會在用戶端電腦上使用 **TreatAs** 所指定的 CLSID 進行。</span><span class="sxs-lookup"><span data-stu-id="3a950-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="3a950-111">DCOM 會查看 **TreatAs** 的本機登錄，即使您呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數並指定遠端伺服器也一樣。</span><span class="sxs-lookup"><span data-stu-id="3a950-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="3a950-112">這表示，如果您有要在本機電腦上將 Class1 視為 Class2 的 **TreatAs** 專案，但您呼叫 **CoCreateInstance** 來建立 Class1 的實例，並指定遠端伺服器，則 DCOM 將會嘗試在遠端伺服器上建立 Class2 的實例，即使 Class2 未在遠端伺服器上註冊，也會導致對 **CoCreateInstance** 的呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="3a950-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a950-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a950-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a950-114">**AutoTreatAs**</span><span class="sxs-lookup"><span data-stu-id="3a950-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="3a950-115">**CoGetTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="3a950-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="3a950-116">**CoTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="3a950-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 





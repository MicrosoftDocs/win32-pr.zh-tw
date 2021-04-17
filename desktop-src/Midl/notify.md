---
title: 通知屬性
description: '\ Notify \ 屬性會指示 MIDL 編譯器在應用程式的伺服器端產生對 \ notify \ 程式的呼叫。'
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- 通知屬性 MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507532"
---
# <a name="notify-attribute"></a><span data-ttu-id="0ac36-104">通知屬性</span><span class="sxs-lookup"><span data-stu-id="0ac36-104">notify attribute</span></span>

<span data-ttu-id="0ac36-105">[ **\[ 通知 \]** ] 屬性會指示 MIDL 編譯器在應用程式的伺服器端產生 **\[ 通知 \]** 程式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0ac36-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="0ac36-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ac36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac36-107">*程式-名稱*</span><span class="sxs-lookup"><span data-stu-id="0ac36-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0ac36-108">將與通知程式相關聯的遠端程式名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac36-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ac36-109">備註</span><span class="sxs-lookup"><span data-stu-id="0ac36-109">Remarks</span></span>

<span data-ttu-id="0ac36-110">[ **\[ 通知 \]** ] 屬性所呼叫的 **\[ 通知 \]** 程式，會與伺服器上的特定遠端程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="0ac36-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="0ac36-111">它類似于回呼函數的概念。</span><span class="sxs-lookup"><span data-stu-id="0ac36-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="0ac36-112">Stub 會在其相關聯的遠端程式的所有輸出引數都經過封送處理，並釋放與參數相關聯的任何記憶體之後，呼叫 **\[ 通知 \]** 程式。</span><span class="sxs-lookup"><span data-stu-id="0ac36-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="0ac36-113">如果呼叫在伺服器常式執行之前失敗，則會呼叫 **\[ 通知 \]** 常式。</span><span class="sxs-lookup"><span data-stu-id="0ac36-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="0ac36-114">例如，如果伺服器因為從用戶端收到不正確的資料而在封送時失敗， \[ 則 \] 會呼叫通知常式。</span><span class="sxs-lookup"><span data-stu-id="0ac36-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="0ac36-115">在遠端程式中開發取得資源的應用程式時，[ **\[ 通知 \]** ] 屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="0ac36-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="0ac36-116">然後，這些資源就會在遠端程式的輸出參數完全封送處理之後，于 **\[ 通知 \]** 程式中釋出。</span><span class="sxs-lookup"><span data-stu-id="0ac36-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="0ac36-117">**\[ 通知 \]** 程式名稱是以 [ **\_ 通知**] 尾碼的遠端程式名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac36-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="0ac36-118">**\_ 通知** 程式不需要任何參數，也不會傳回結果。</span><span class="sxs-lookup"><span data-stu-id="0ac36-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="0ac36-119">這項程式的原型也會在標頭檔中產生。</span><span class="sxs-lookup"><span data-stu-id="0ac36-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="0ac36-120">例如，如果 IDL 檔案包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="0ac36-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="0ac36-121">在 ACF for MIDL 中指定下列各項，以產生 **\_ 通知** 呼叫：</span><span class="sxs-lookup"><span data-stu-id="0ac36-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="0ac36-122">MIDL 編譯器將會產生包含下列 **\_ 通知** 程式呼叫的伺服器 stub 程式碼：</span><span class="sxs-lookup"><span data-stu-id="0ac36-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="0ac36-123">標頭檔將包含原型：</span><span class="sxs-lookup"><span data-stu-id="0ac36-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="0ac36-124">範例</span><span class="sxs-lookup"><span data-stu-id="0ac36-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="0ac36-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ac36-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac36-126">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="0ac36-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 





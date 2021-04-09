---
title: 隱含與明確的控制碼
description: 若要宣告序列化控制碼，請使用基本控制碼類型 handle \_ t。
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842615"
---
# <a name="implicit-vs-explicit-handles"></a><span data-ttu-id="d7126-103">隱含與明確的控制碼</span><span class="sxs-lookup"><span data-stu-id="d7126-103">Implicit vs. Explicit Handles</span></span>

<span data-ttu-id="d7126-104">若要宣告序列化控制碼，請使用基本控制碼類型 [**handle \_ t**](/windows/desktop/Midl/handle-t)。</span><span class="sxs-lookup"><span data-stu-id="d7126-104">To declare a serialization handle, use the primitive handle type [**handle\_t**](/windows/desktop/Midl/handle-t).</span></span> <span data-ttu-id="d7126-105">序列化控制碼可以是明確或隱含的。</span><span class="sxs-lookup"><span data-stu-id="d7126-105">Serialization handles can be explicit or implicit.</span></span> <span data-ttu-id="d7126-106">使用 **\[ 隱含 \_ 控制碼 \]** 屬性，在應用程式的 ACF 中指定隱含控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7126-106">Specify implicit handles in your application's ACF by using the **\[implicit\_handle\]** attribute.</span></span> <span data-ttu-id="d7126-107">MIDL 編譯器將會產生全域序列化控制碼變數。</span><span class="sxs-lookup"><span data-stu-id="d7126-107">The MIDL compiler will generate a global serialization handle variable.</span></span> <span data-ttu-id="d7126-108">具有隱含控制碼的序列化程式會使用這個全域變數來存取有效的序列化內容。</span><span class="sxs-lookup"><span data-stu-id="d7126-108">Serialization procedures with an implicit handle use this global variable in order to access a valid serializing context.</span></span>

<span data-ttu-id="d7126-109">使用類型編碼時，產生的常式支援特定型別的序列化，會使用全域隱含控制碼來存取序列化內容。</span><span class="sxs-lookup"><span data-stu-id="d7126-109">When using type encoding, the generated routines supporting serialization of a particular type use the global implicit handle to access the serialization context.</span></span> <span data-ttu-id="d7126-110">請注意，遠端常式可能需要使用隱含控制碼作為系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7126-110">Note that remote routines may need to use the implicit handle as a binding handle.</span></span> <span data-ttu-id="d7126-111">在進行序列化呼叫之前，請確定隱含控制碼已設定為有效的序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7126-111">Be sure that the implicit handle is set to a valid serializing handle prior to making a serializing call.</span></span>

<span data-ttu-id="d7126-112">明確的控制碼會指定為 IDL 檔案中序列化程式原型的參數，或者也可以使用 ACF 中的 **\[ 明確 \_ 控制碼 \]** 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="d7126-112">An explicit handle is specified as a parameter of the serialization procedure prototype in the IDL file, or it can also be specified by using the **\[explicit\_handle\]** attribute in the ACF.</span></span> <span data-ttu-id="d7126-113">明確控制碼參數是用來建立程式的適當序列化內容。</span><span class="sxs-lookup"><span data-stu-id="d7126-113">The explicit handle parameter is used to establish the proper serialization context for the procedure.</span></span> <span data-ttu-id="d7126-114">為了在序列化類型的情況下建立正確的內容，編譯器會產生使用明確 [**控制碼 \_ t**](/windows/desktop/Midl/handle-t) 參數作為序列化控制碼的支援常式。</span><span class="sxs-lookup"><span data-stu-id="d7126-114">To establish the correct context in the case of type serialization, the compiler generates the supporting routines that use explicit [**handle\_t**](/windows/desktop/Midl/handle-t) parameter as the serialization handle.</span></span> <span data-ttu-id="d7126-115">呼叫序列化程式或序列化型別支援常式時，必須提供有效的序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7126-115">You must supply a valid serializing handle when calling a serialization procedure or serialization type support routine.</span></span>

 

 
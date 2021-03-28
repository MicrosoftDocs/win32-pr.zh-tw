---
title: '暫存註冊 (HLSL 與參考) '
description: 頂點著色器暫存登錄用來保存中繼結果。
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313797"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="31a15-103">暫存註冊 (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="31a15-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="31a15-104">頂點著色器暫存登錄用來保存中繼結果。</span><span class="sxs-lookup"><span data-stu-id="31a15-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="31a15-105">在使用暫存登錄之前，必須先將它初始化。</span><span class="sxs-lookup"><span data-stu-id="31a15-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="31a15-106">每個暫存登錄都具有單一寫入和三次讀取的存取權。</span><span class="sxs-lookup"><span data-stu-id="31a15-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="31a15-107">這表示單一著色器指令最多可使用三個暫存暫存器做為輸入。</span><span class="sxs-lookup"><span data-stu-id="31a15-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="31a15-108">無法使用在先前叫用端點著色器之前保持的臨時暫存器值。</span><span class="sxs-lookup"><span data-stu-id="31a15-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="31a15-109">暫存器包含的屬性會決定每個註冊的行為。</span><span class="sxs-lookup"><span data-stu-id="31a15-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="31a15-110">屬性</span><span class="sxs-lookup"><span data-stu-id="31a15-110">Property</span></span>        | <span data-ttu-id="31a15-111">描述</span><span class="sxs-lookup"><span data-stu-id="31a15-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a15-112">Name</span><span class="sxs-lookup"><span data-stu-id="31a15-112">Name</span></span>            | <span data-ttu-id="31a15-113">r \[ n \] 。</span><span class="sxs-lookup"><span data-stu-id="31a15-113">r\[n\].</span></span> <span data-ttu-id="31a15-114">n 是選擇性的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="31a15-114">n is an optional register number.</span></span> <span data-ttu-id="31a15-115">預設值為0，如果未指定任何值，則為所使用的值。</span><span class="sxs-lookup"><span data-stu-id="31a15-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="31a15-116">Count</span><span class="sxs-lookup"><span data-stu-id="31a15-116">Count</span></span>           | <span data-ttu-id="31a15-117">最多12個註冊程式。</span><span class="sxs-lookup"><span data-stu-id="31a15-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="31a15-118">I/o 許可權</span><span class="sxs-lookup"><span data-stu-id="31a15-118">I/O permissions</span></span> | <span data-ttu-id="31a15-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="31a15-119">Read/write.</span></span> <span data-ttu-id="31a15-120">此暫存器可由 API 或著色器讀取或寫入。</span><span class="sxs-lookup"><span data-stu-id="31a15-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="31a15-121">讀取埠</span><span class="sxs-lookup"><span data-stu-id="31a15-121">Read ports</span></span>      | <span data-ttu-id="31a15-122">在單一指令中可讀取的暫存器次數為3。</span><span class="sxs-lookup"><span data-stu-id="31a15-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="31a15-123">臨時暫存器是唯一可在單一指令中讀取和寫入一次以上的暫存器。</span><span class="sxs-lookup"><span data-stu-id="31a15-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="31a15-124">每個暫存登錄都具有單一寫入和三次讀取的存取權。</span><span class="sxs-lookup"><span data-stu-id="31a15-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="31a15-125">因此，指令在一組輸入來源運算元中最多可以有三個暫存暫存器。</span><span class="sxs-lookup"><span data-stu-id="31a15-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="31a15-126">臨時暫存器中的任何值都不能使用先前調用的端點著色器。</span><span class="sxs-lookup"><span data-stu-id="31a15-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="31a15-127">在寫入之前從暫時登錄讀取值的頂點著色器將會使 Direct3D API 呼叫無法建立頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="31a15-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="31a15-128">範例</span><span class="sxs-lookup"><span data-stu-id="31a15-128">Example</span></span>

<span data-ttu-id="31a15-129">以下是使用暫存註冊的範例：</span><span class="sxs-lookup"><span data-stu-id="31a15-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="31a15-130">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="31a15-130">Vertex shader versions</span></span> | <span data-ttu-id="31a15-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="31a15-131">1\_1</span></span> | <span data-ttu-id="31a15-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31a15-132">2\_0</span></span> | <span data-ttu-id="31a15-133">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="31a15-133">2\_sw</span></span> | <span data-ttu-id="31a15-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31a15-134">2\_x</span></span> | <span data-ttu-id="31a15-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31a15-135">3\_0</span></span> | <span data-ttu-id="31a15-136">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="31a15-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="31a15-137">暫時註冊</span><span class="sxs-lookup"><span data-stu-id="31a15-137">Temporary Register</span></span>     | <span data-ttu-id="31a15-138">x</span><span class="sxs-lookup"><span data-stu-id="31a15-138">x</span></span>    | <span data-ttu-id="31a15-139">x</span><span class="sxs-lookup"><span data-stu-id="31a15-139">x</span></span>    | <span data-ttu-id="31a15-140">x</span><span class="sxs-lookup"><span data-stu-id="31a15-140">x</span></span>     | <span data-ttu-id="31a15-141">x</span><span class="sxs-lookup"><span data-stu-id="31a15-141">x</span></span>    | <span data-ttu-id="31a15-142">x</span><span class="sxs-lookup"><span data-stu-id="31a15-142">x</span></span>    | <span data-ttu-id="31a15-143">x</span><span class="sxs-lookup"><span data-stu-id="31a15-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="31a15-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="31a15-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31a15-145">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="31a15-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





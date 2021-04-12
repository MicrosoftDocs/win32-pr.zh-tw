---
title: 常見的編譯器錯誤
description: 本節說明在遷移現有的程式碼基底時，所發生的一般編譯器錯誤。 這些範例是來自系統層級的 HAL 程式碼，雖然這些概念直接適用于使用者層級程式碼。
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- 編譯器錯誤 64-位 Windows 程式設計
- 遷移64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316804"
---
# <a name="common-compiler-errors"></a><span data-ttu-id="403fd-106">常見的編譯器錯誤</span><span class="sxs-lookup"><span data-stu-id="403fd-106">Common Compiler Errors</span></span>

<span data-ttu-id="403fd-107">本節說明在遷移現有的程式碼基底時，所發生的一般編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="403fd-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="403fd-108">這些範例是來自系統層級的 HAL 程式碼，雖然這些概念直接適用于使用者層級程式碼。</span><span class="sxs-lookup"><span data-stu-id="403fd-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="403fd-109">警告 C4311 範例1</span><span class="sxs-lookup"><span data-stu-id="403fd-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="403fd-110">' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="403fd-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="403fd-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-113">**PtrToUlong** 是內嵌函數或宏，視您的使用方式而定。</span><span class="sxs-lookup"><span data-stu-id="403fd-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="403fd-114">它會截斷指向 **ULONG** 的指標。</span><span class="sxs-lookup"><span data-stu-id="403fd-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="403fd-115">雖然32位指標不受影響，但64位指標的上半部會被截斷。</span><span class="sxs-lookup"><span data-stu-id="403fd-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="403fd-116">CIA \_ PCI \_ CONFIG \_ BASE \_ QVA 宣告為 **PVOID**。</span><span class="sxs-lookup"><span data-stu-id="403fd-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="403fd-117">**ULONG** 轉換適用于32位世界，但在64位世界中會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="403fd-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="403fd-118">解決方法是取得 **ULONG** 的64位指標，因為變更 pPciAddr->u. AsULONG 的聯集定義在變更太多程式碼中定義。</span><span class="sxs-lookup"><span data-stu-id="403fd-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="403fd-119">您可以使用宏 **PtrToUlong** 將64位 **PVOID** 轉換成所需的 **ULONG** ，因為我們知道 CIA \_ PCI \_ CONFIG \_ BASE \_ QVA 的特定值。</span><span class="sxs-lookup"><span data-stu-id="403fd-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="403fd-120">在此情況下，此指標將永遠不會有最高32位中的資料。</span><span class="sxs-lookup"><span data-stu-id="403fd-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="403fd-122">警告 C4311 範例2</span><span class="sxs-lookup"><span data-stu-id="403fd-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="403fd-123">' type cast '：從 ' struct \_ ERROR \_ FRAME \* \_ \_ ptr64 ' 到 ' 不帶正負號的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="403fd-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="403fd-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-126">問題在於，此函式的最後一個參數是資料結構的指標。</span><span class="sxs-lookup"><span data-stu-id="403fd-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="403fd-127">因為 PUncorrectableError 是指標，所以會使用程式設計模型來變更大小。</span><span class="sxs-lookup"><span data-stu-id="403fd-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="403fd-128">**KeBugCheckEx** 的原型已變更，因此最後一個參數為 **ULONG \_ PTR**。</span><span class="sxs-lookup"><span data-stu-id="403fd-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="403fd-129">因此，必須將函式指標轉型為 **ULONG \_ PTR**。</span><span class="sxs-lookup"><span data-stu-id="403fd-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="403fd-130">您可能會問：為什麼不使用 **PVOID** 做為最後一個參數。</span><span class="sxs-lookup"><span data-stu-id="403fd-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="403fd-131">視呼叫的內容而定，最後一個參數可能是指標以外的內容，或可能是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="403fd-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="403fd-133">警告 C4244 範例1</span><span class="sxs-lookup"><span data-stu-id="403fd-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="403fd-134">' = '：從 ' struct \_ configuration \_ component \* \_ \_ ptr64 ' 轉換為 ' struct \_ configuration \_ component \* '，可能遺失資料</span><span class="sxs-lookup"><span data-stu-id="403fd-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="403fd-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="403fd-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-137">函數會將變數元件宣告為 PCONFIGURATION \_ 元件。</span><span class="sxs-lookup"><span data-stu-id="403fd-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="403fd-138">之後，此變數會在下列正確的指派中使用：</span><span class="sxs-lookup"><span data-stu-id="403fd-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="403fd-139">不過，類型 PCONFIGURATION \_ 元件定義如下：</span><span class="sxs-lookup"><span data-stu-id="403fd-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="403fd-140">PCONFIGURATION 元件的型別定義 \_ 會在32位和64位模型中提供32位指標，因為它是宣告的 **指標 \_ 32**。</span><span class="sxs-lookup"><span data-stu-id="403fd-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="403fd-141">此結構的原始設計工具知道它即將用於 BIOS 中的32位內容，並明確地加以定義以供使用。</span><span class="sxs-lookup"><span data-stu-id="403fd-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="403fd-142">這段程式碼在32位視窗中運作正常，因為指標會是32位。</span><span class="sxs-lookup"><span data-stu-id="403fd-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="403fd-143">在64位的 Windows 中，它無法運作，因為程式碼是在64位內容中。</span><span class="sxs-lookup"><span data-stu-id="403fd-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="403fd-145">若要解決這個問題，請使用設定 \_ 元件， \* 而不是32位的 PCONFIGURATION \_ 元件。</span><span class="sxs-lookup"><span data-stu-id="403fd-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="403fd-146">務必清楚瞭解程式碼的用途。</span><span class="sxs-lookup"><span data-stu-id="403fd-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="403fd-147">如果此程式碼的目的是要接觸32位的 BIOS 或系統空間，此修正程式將無法運作。</span><span class="sxs-lookup"><span data-stu-id="403fd-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="403fd-148">**指標 \_ 32** 定義于 Ntdef 和 Winnt. h 中。</span><span class="sxs-lookup"><span data-stu-id="403fd-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="403fd-149">警告 C4242 範例2</span><span class="sxs-lookup"><span data-stu-id="403fd-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="403fd-150">' = '：從 ' \_ \_ int64 ' 轉換成「不帶正負號的長時間」，可能遺失資料</span><span class="sxs-lookup"><span data-stu-id="403fd-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="403fd-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span data-ttu-id="403fd-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-153">產生此警告的原因是，計算使用的是64位值，在本例中為指標，並將結果放在32位的 **ULONG** 中。</span><span class="sxs-lookup"><span data-stu-id="403fd-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="403fd-155">將計算的結果型別轉換為 **ULONG** ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="403fd-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="403fd-156">Typecasting 結果可讓編譯器知道您確定結果。</span><span class="sxs-lookup"><span data-stu-id="403fd-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="403fd-157">話雖如此，請確定您瞭解這項計算，並確實確定它能符合32位的 **ULONG**。</span><span class="sxs-lookup"><span data-stu-id="403fd-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="403fd-158">如果結果可能無法容納在32位的 **ULONG** 中，請變更將保留結果之變數的基底類型。</span><span class="sxs-lookup"><span data-stu-id="403fd-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="403fd-159">警告 C4311-範例1</span><span class="sxs-lookup"><span data-stu-id="403fd-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="403fd-160">' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="403fd-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span data-ttu-id="403fd-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-163">整個函式會以整數的形式處理位址，強制需要以可移植的方式輸入這些整數。</span><span class="sxs-lookup"><span data-stu-id="403fd-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="403fd-164">所有區域變數、計算和傳回值中的中繼值都應該是可移植類型。</span><span class="sxs-lookup"><span data-stu-id="403fd-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

<span data-ttu-id="403fd-166">**PULONG \_PTR** 是適用于32位 windows 和64位（適用于64位 windows）本身32位的指標。</span><span class="sxs-lookup"><span data-stu-id="403fd-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="403fd-167">它會指向不帶正負號的整數（ **ULONG \_ PTR**），也就是32位 windows 的32位和64位 windows 的64位。</span><span class="sxs-lookup"><span data-stu-id="403fd-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="403fd-168">警告 C4311-範例2</span><span class="sxs-lookup"><span data-stu-id="403fd-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="403fd-169">' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="403fd-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span data-ttu-id="403fd-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-172">即使所有 QVA (好用的虛擬位址) 值在這個階段是真正的32位值，而且將符合 **ulong**，但在可能的情況下，將所有位址視為 **ulong \_ PTR** 值會更一致。</span><span class="sxs-lookup"><span data-stu-id="403fd-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="403fd-173">指標 PciIoSpaceBase 會保留在宏 HAL 中建立的 QVA \_ 建立 \_ QVA。</span><span class="sxs-lookup"><span data-stu-id="403fd-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="403fd-174">此宏會傳回64位值，其中 top 32 位設為零，因此數學運算將會運作。</span><span class="sxs-lookup"><span data-stu-id="403fd-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="403fd-175">我們可以直接讓程式碼將指標截斷為 **ULONG**，但不建議您這麼做，以增強程式碼可維護性和可攜性。</span><span class="sxs-lookup"><span data-stu-id="403fd-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="403fd-176">例如，QVA 的內容可能會在未來變更，以使用此層級的部分上層，以中斷程式碼。</span><span class="sxs-lookup"><span data-stu-id="403fd-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="403fd-178">請放心，並針對所有位址和指標數學使用 **ULONG \_ PTR** 。</span><span class="sxs-lookup"><span data-stu-id="403fd-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="403fd-179">警告 C4311 範例3</span><span class="sxs-lookup"><span data-stu-id="403fd-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="403fd-180">' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="403fd-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span data-ttu-id="403fd-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-183">如果套用到指標類型，則編譯器會警告 (&) 和左移 (<<) 運算子的位址。</span><span class="sxs-lookup"><span data-stu-id="403fd-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="403fd-184">在上述程式碼中，Qva 是 **PVOID** 值。</span><span class="sxs-lookup"><span data-stu-id="403fd-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="403fd-185">我們必須將其轉換成整數類型，才能執行數學運算。</span><span class="sxs-lookup"><span data-stu-id="403fd-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="403fd-186">因為此程式碼必須是可移植的，所以請使用 **ulong \_ PTR** 而非 **ulong**。</span><span class="sxs-lookup"><span data-stu-id="403fd-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="403fd-188">警告 C4311 範例4</span><span class="sxs-lookup"><span data-stu-id="403fd-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="403fd-189">' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="403fd-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="403fd-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-192">TranslatedAddress 是如下所示的聯集：</span><span class="sxs-lookup"><span data-stu-id="403fd-192">TranslatedAddress is a union that looks something like the following:</span></span>

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span data-ttu-id="403fd-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="403fd-194">知道程式碼的其餘部分可能會放在 Highpart 中，我們可以選取其中一個顯示的解決方案。</span><span class="sxs-lookup"><span data-stu-id="403fd-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="403fd-195">**PtrToUlong** 宏會將 **HalCreateQva** 傳回的指標截斷為32位。</span><span class="sxs-lookup"><span data-stu-id="403fd-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="403fd-196">我們知道 **HalCreateQva** 所傳回的 QVA 會將上半部32位設為零，而下一行程式碼會將 TranslatedAddress->Highpart 為零。</span><span class="sxs-lookup"><span data-stu-id="403fd-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="403fd-197">請注意，我們可以使用下列各項：</span><span class="sxs-lookup"><span data-stu-id="403fd-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="403fd-198">這適用于此範例： **HalCreateQva** 宏會傳回64位，其中的32位設定為零。</span><span class="sxs-lookup"><span data-stu-id="403fd-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="403fd-199">請特別注意，不要在32位環境中保留未定義的32位，這第二個解決方案可能真的會這樣做。</span><span class="sxs-lookup"><span data-stu-id="403fd-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="403fd-200">警告 C4311 範例5</span><span class="sxs-lookup"><span data-stu-id="403fd-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="403fd-201">' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷</span><span class="sxs-lookup"><span data-stu-id="403fd-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="403fd-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼</span><span class="sxs-lookup"><span data-stu-id="403fd-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span data-ttu-id="403fd-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="403fd-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="403fd-204">WindowRegisters->WindowBase 是指標，現在是64位。</span><span class="sxs-lookup"><span data-stu-id="403fd-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="403fd-205">這段程式碼會將此值以滑鼠右鍵右移20位。</span><span class="sxs-lookup"><span data-stu-id="403fd-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="403fd-206">編譯器不會讓我們在指標上使用右移 (>>) 運算子;因此，我們需要將它轉換成某種整數。</span><span class="sxs-lookup"><span data-stu-id="403fd-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="403fd-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案</span><span class="sxs-lookup"><span data-stu-id="403fd-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="403fd-208">轉型為 **ULONG \_ PTR** 正是我們所需要的。</span><span class="sxs-lookup"><span data-stu-id="403fd-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="403fd-209">下一個問題是 Wbase。</span><span class="sxs-lookup"><span data-stu-id="403fd-209">The next problem is Wbase.</span></span> <span data-ttu-id="403fd-210">Wbase 為 **ULONG** 且為32位。</span><span class="sxs-lookup"><span data-stu-id="403fd-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="403fd-211">在此情況下，我們知道64位指標 WindowRegisters->WindowBase 在較低的32位中是有效的，即使在移動之後也是如此。</span><span class="sxs-lookup"><span data-stu-id="403fd-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="403fd-212">這會讓 **PtrToUlong** 宏可接受使用，因為它會將64位指標截斷為32位的 **ULONG**。</span><span class="sxs-lookup"><span data-stu-id="403fd-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="403fd-213">**PVOID** 轉換是必要的，因為 **PtrToUlong** 需要指標引數。</span><span class="sxs-lookup"><span data-stu-id="403fd-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="403fd-214">當您查看所產生的組合器程式碼時，所有的 C 程式碼轉換都只會變成負載四、右移和儲存時間。</span><span class="sxs-lookup"><span data-stu-id="403fd-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 





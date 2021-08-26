---
title: 常見的編譯器錯誤
description: 本節說明在遷移現有的程式碼基底時，所發生的一般編譯器錯誤。 這些範例是來自系統層級的 HAL 程式碼，雖然這些概念直接適用于使用者層級程式碼。
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- 編譯器錯誤 64-位 Windows 程式設計
- 遷移64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d12e7c5566b5cb2b934eefb71b1b51858f278d3e408d3080cb1810f185dcfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071638"
---
# <a name="common-compiler-errors"></a>常見的編譯器錯誤

本節說明在遷移現有的程式碼基底時，所發生的一般編譯器錯誤。 這些範例是來自系統層級的 HAL 程式碼，雖然這些概念直接適用于使用者層級程式碼。

## <a name="warning-c4311-example-1"></a>警告 C4311 範例1

' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

**PtrToUlong** 是內嵌函數或宏，視您的使用方式而定。 它會截斷指向 **ULONG** 的指標。 雖然32位指標不受影響，但64位指標的上半部會被截斷。

CIA \_ PCI \_ CONFIG \_ BASE \_ QVA 宣告為 **PVOID**。 **ULONG** 轉換適用于32位世界，但在64位世界中會導致錯誤。 解決方法是取得 **ULONG** 的64位指標，因為變更 pPciAddr->u. AsULONG 的聯集定義在變更太多程式碼中定義。

您可以使用宏 **PtrToUlong** 將64位 **PVOID** 轉換成所需的 **ULONG** ，因為我們知道 CIA \_ PCI \_ CONFIG \_ BASE \_ QVA 的特定值。 在此情況下，此指標將永遠不會有最高32位中的資料。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>警告 C4311 範例2

' type cast '：從 ' struct \_ ERROR \_ FRAME \* \_ \_ ptr64 ' 到 ' 不帶正負號的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

問題在於，此函式的最後一個參數是資料結構的指標。 因為 PUncorrectableError 是指標，所以會使用程式設計模型來變更大小。 **KeBugCheckEx** 的原型已變更，因此最後一個參數為 **ULONG \_ PTR**。 因此，必須將函式指標轉型為 **ULONG \_ PTR**。

您可能會問：為什麼不使用 **PVOID** 做為最後一個參數。 視呼叫的內容而定，最後一個參數可能是指標以外的內容，或可能是錯誤碼。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>警告 C4244 範例1

' = '：從 ' struct \_ configuration \_ component \* \_ \_ ptr64 ' 轉換為 ' struct \_ configuration \_ component \* '，可能遺失資料

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

函數會將變數元件宣告為 PCONFIGURATION \_ 元件。 之後，此變數會在下列正確的指派中使用：

`Component = &CurrentEntry->ComponentEntry;`

不過，類型 PCONFIGURATION \_ 元件定義如下：

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

PCONFIGURATION 元件的型別定義 \_ 會在32位和64位模型中提供32位指標，因為它是宣告的 **指標 \_ 32**。 此結構的原始設計工具知道它即將用於 BIOS 中的32位內容，並明確地加以定義以供使用。 這段程式碼在32位 Windows 中運作正常，因為指標會是32位。 在64位 Windows 中，它無法運作，因為程式碼是在64位內容中。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

若要解決這個問題，請使用設定 \_ 元件， \* 而不是32位的 PCONFIGURATION \_ 元件。 務必清楚瞭解程式碼的用途。 如果此程式碼的目的是要接觸32位的 BIOS 或系統空間，此修正程式將無法運作。

**指標 \_ 32** 定義于 Ntdef 和 Winnt. h 中。

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>警告 C4242 範例2

' = '：從 ' \_ \_ int64 ' 轉換成「不帶正負號的長時間」，可能遺失資料

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

產生此警告的原因是，計算使用的是64位值，在本例中為指標，並將結果放在32位的 **ULONG** 中。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

將計算的結果型別轉換為 **ULONG** ，如下所示：

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Typecasting 結果可讓編譯器知道您確定結果。 話雖如此，請確定您瞭解這項計算，並確實確定它能符合32位的 **ULONG**。

如果結果可能無法容納在32位的 **ULONG** 中，請變更將保留結果之變數的基底類型。

</dd> </dl>

## <a name="warning-c4311---example-1"></a>警告 C4311-範例1

' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

整個函式會以整數的形式處理位址，強制需要以可移植的方式輸入這些整數。 所有區域變數、計算和傳回值中的中繼值都應該是可移植類型。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
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

**PULONG \_PTR** 是一個指標，它本身是32位 Windows 的32位和64位 Windows 的64位。 它會指向不帶正負號的整數（ **ULONG \_ PTR**），也就是32位 Windows 的32位和64位 Windows 的64位。

</dd> </dl>

## <a name="warning-c4311---example-2"></a>警告 C4311-範例2

' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

即使所有 QVA (好用的虛擬位址) 值在這個階段是真正的32位值，而且將符合 **ulong**，但在可能的情況下，將所有位址視為 **ulong \_ PTR** 值會更一致。

指標 PciIoSpaceBase 會保留在宏 HAL 中建立的 QVA \_ 建立 \_ QVA。 此宏會傳回64位值，其中 top 32 位設為零，因此數學運算將會運作。 我們可以直接讓程式碼將指標截斷為 **ULONG**，但不建議您這麼做，以增強程式碼可維護性和可攜性。 例如，QVA 的內容可能會在未來變更，以使用此層級的部分上層，以中斷程式碼。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

請放心，並針對所有位址和指標數學使用 **ULONG \_ PTR** 。

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>警告 C4311 範例3

' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

如果套用到指標類型，則編譯器會警告 (&) 和左移 (<<) 運算子的位址。 在上述程式碼中，Qva 是 **PVOID** 值。 我們必須將其轉換成整數類型，才能執行數學運算。 因為此程式碼必須是可移植的，所以請使用 **ulong \_ PTR** 而非 **ulong**。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>警告 C4311 範例4

' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

TranslatedAddress 是如下所示的聯集：

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

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

知道程式碼的其餘部分可能會放在 Highpart 中，我們可以選取其中一個顯示的解決方案。

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

**PtrToUlong** 宏會將 **HalCreateQva** 傳回的指標截斷為32位。 我們知道 **HalCreateQva** 所傳回的 QVA 會將上半部32位設為零，而下一行程式碼會將 TranslatedAddress->Highpart 為零。

請注意，我們可以使用下列各項：

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

這適用于此範例： **HalCreateQva** 宏會傳回64位，其中的32位設定為零。 請特別注意，不要在32位環境中保留未定義的32位，這第二個解決方案可能真的會這樣做。

</dd> </dl>

## <a name="warning-c4311-example-5"></a>警告 C4311 範例5

' type cast '：從 ' void \* \_ \_ ptr64 ' 到 ' 不帶正負號的長度 ' 的指標截斷

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

WindowRegisters->WindowBase 是指標，現在是64位。 這段程式碼會將此值以滑鼠右鍵右移20位。 編譯器不會讓我們在指標上使用右移 (>>) 運算子;因此，我們需要將它轉換成某種整數。

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>解決 方案
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

轉型為 **ULONG \_ PTR** 正是我們所需要的。 下一個問題是 Wbase。 Wbase 為 **ULONG** 且為32位。 在此情況下，我們知道64位指標 WindowRegisters->WindowBase 在較低的32位中是有效的，即使在移動之後也是如此。 這會讓 **PtrToUlong** 宏可接受使用，因為它會將64位指標截斷為32位的 **ULONG**。 **PVOID** 轉換是必要的，因為 **PtrToUlong** 需要指標引數。 當您查看所產生的組合器程式碼時，所有的 C 程式碼轉換都只會變成負載四、右移和儲存時間。

</dd> </dl>

 

 





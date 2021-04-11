---
description: Win32 \_ SERIALPORTCONFIGURATION WMI 類別代表以 Windows 為基礎之序列埠上的資料傳輸設定。 這包括建立連接和錯誤檢查的設定。
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936109"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="86861-104">Win32 \_ SerialPortConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="86861-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="86861-105">**Win32 \_ SerialPortConfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表以 Windows 為基礎之序列埠上的資料傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="86861-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="86861-106">這包括建立連接和錯誤檢查的設定。</span><span class="sxs-lookup"><span data-stu-id="86861-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="86861-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="86861-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="86861-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="86861-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86861-109">語法</span><span class="sxs-lookup"><span data-stu-id="86861-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="86861-110">成員</span><span class="sxs-lookup"><span data-stu-id="86861-110">Members</span></span>

<span data-ttu-id="86861-111">**Win32 \_ SerialPortConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86861-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="86861-112">屬性</span><span class="sxs-lookup"><span data-stu-id="86861-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86861-113">屬性</span><span class="sxs-lookup"><span data-stu-id="86861-113">Properties</span></span>

<span data-ttu-id="86861-114">**Win32 \_ SerialPortConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86861-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86861-115">**AbortReadWriteOnError**</span><span class="sxs-lookup"><span data-stu-id="86861-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-118">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError" ) </span><span class="sxs-lookup"><span data-stu-id="86861-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="86861-119">若 **為 TRUE**，則會在發生錯誤時終止讀取和寫入作業。</span><span class="sxs-lookup"><span data-stu-id="86861-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="86861-120">若 **為 TRUE**，當發生錯誤時，驅動程式會終止所有的讀取和寫入作業，並顯示錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="86861-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="86861-121">在應用程式確認錯誤之前，驅動程式將不會接受任何進一步的通訊作業。</span><span class="sxs-lookup"><span data-stu-id="86861-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="86861-122">**串列傳輸速率**</span><span class="sxs-lookup"><span data-stu-id="86861-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-125">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| 串列傳輸速率" ) </span><span class="sxs-lookup"><span data-stu-id="86861-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="86861-126">每秒傳輸 (位數) 通訊裝置運作的速率。</span><span class="sxs-lookup"><span data-stu-id="86861-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="86861-127">範例：9600</span><span class="sxs-lookup"><span data-stu-id="86861-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="86861-128">**BinaryModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="86861-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-131">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary" ) </span><span class="sxs-lookup"><span data-stu-id="86861-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="86861-132">若 **為 TRUE**，則會啟用序列埠的二進位模式資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="86861-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="86861-133">執行 Windows 的電腦系統只允許透過序列埠進行二進位傳輸，因此這個值一律 **為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="86861-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="86861-134">**BitsPerByte**</span><span class="sxs-lookup"><span data-stu-id="86861-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-137">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize" ) </span><span class="sxs-lookup"><span data-stu-id="86861-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="86861-138">Windows 序列埠的每個位元組資料傳輸和接收的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="86861-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="86861-139">此數目可能會隨著控制項和錯誤更正位（例如同位檢查位）而有所不同。</span><span class="sxs-lookup"><span data-stu-id="86861-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="86861-140">範例：8</span><span class="sxs-lookup"><span data-stu-id="86861-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="86861-141">**標題**</span><span class="sxs-lookup"><span data-stu-id="86861-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-144">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="86861-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="86861-145">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="86861-145">Short textual description of the current object.</span></span>

<span data-ttu-id="86861-146">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="86861-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="86861-147">**ContinueXMitOnXOff**</span><span class="sxs-lookup"><span data-stu-id="86861-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-150">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff" ) </span><span class="sxs-lookup"><span data-stu-id="86861-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="86861-151">若 **為 TRUE**，當輸入緩衝區在 **XOffXMitThreshold** 個位元組內已滿，且驅動程式已傳送 **XOffChararcter** 值以停止接收位元組時，資料傳輸會繼續。</span><span class="sxs-lookup"><span data-stu-id="86861-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="86861-152">若 **為 FALSE**，則在輸入緩衝區在 **XOnXMitThreshold** 個位元組內為空白且驅動程式已傳送 **XOnCharacter** 值以繼續接收之前，傳輸將無法繼續。</span><span class="sxs-lookup"><span data-stu-id="86861-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="86861-153">**CTSOutflowControl**</span><span class="sxs-lookup"><span data-stu-id="86861-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-154">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-156">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow" ) </span><span class="sxs-lookup"><span data-stu-id="86861-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="86861-157">若為 **TRUE**，則會在傳輸資料之前，先檢查要傳送 (CTS 的 clear) 信號。</span><span class="sxs-lookup"><span data-stu-id="86861-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="86861-158">CTS 表示序列連接上的兩部裝置都已準備好傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="86861-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="86861-159">資料傳輸會暫止，直到獲得 CTS 信號為止。</span><span class="sxs-lookup"><span data-stu-id="86861-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="86861-160">**說明**</span><span class="sxs-lookup"><span data-stu-id="86861-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86861-163">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="86861-163">Textual description of the current object.</span></span>

<span data-ttu-id="86861-164">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="86861-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="86861-165">**DiscardNullBytes**</span><span class="sxs-lookup"><span data-stu-id="86861-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-166">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-168">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull" ) </span><span class="sxs-lookup"><span data-stu-id="86861-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="86861-169">若 **為 TRUE**，則會在收到 **Null** 位元組後將其捨棄 (的字元) 。</span><span class="sxs-lookup"><span data-stu-id="86861-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="86861-170">**DSROutflowControl**</span><span class="sxs-lookup"><span data-stu-id="86861-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-171">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-173">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow" ) </span><span class="sxs-lookup"><span data-stu-id="86861-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="86861-174">若為 **TRUE**，當資料集就緒 (DSR) 條件時，便會啟用資料流程控制。</span><span class="sxs-lookup"><span data-stu-id="86861-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="86861-175">DSR 表示連接已由序列連接上的裝置所建立。</span><span class="sxs-lookup"><span data-stu-id="86861-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="86861-176">DSR 資料傳輸會暫止，直到指定 DSR 信號為止。</span><span class="sxs-lookup"><span data-stu-id="86861-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="86861-177">**DSRSensitivity**</span><span class="sxs-lookup"><span data-stu-id="86861-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-178">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-180">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity" ) </span><span class="sxs-lookup"><span data-stu-id="86861-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="86861-181">若 **為 TRUE**，則表示通訊驅動程式會區分 DSR 信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="86861-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="86861-182">除非 DSR 數據機輸入行很高，否則驅動程式會忽略任何收到的位元組。</span><span class="sxs-lookup"><span data-stu-id="86861-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="86861-183">**DTRFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="86861-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-186">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl" ) </span><span class="sxs-lookup"><span data-stu-id="86861-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="86861-187">建立連線之後，使用資料終端機 (DTR) 流量控制。</span><span class="sxs-lookup"><span data-stu-id="86861-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="86861-188">**啟用** ( "enable" ) </span><span class="sxs-lookup"><span data-stu-id="86861-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="86861-189">**停** 用 ( 「停用」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="86861-190">**交握** ( 「交握」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86861-191">**EOFCharacter**</span><span class="sxs-lookup"><span data-stu-id="86861-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-192">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-194">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar" ) </span><span class="sxs-lookup"><span data-stu-id="86861-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="86861-195">用來表示資料結尾的字元值。</span><span class="sxs-lookup"><span data-stu-id="86861-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="86861-196">範例： ^ Z</span><span class="sxs-lookup"><span data-stu-id="86861-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="86861-197">**ErrorReplaceCharacter**</span><span class="sxs-lookup"><span data-stu-id="86861-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-198">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-200">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar" ) </span><span class="sxs-lookup"><span data-stu-id="86861-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="86861-201">用來取代以同位檢查錯誤接收之位元組的字元值。</span><span class="sxs-lookup"><span data-stu-id="86861-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="86861-202">範例： ^ C</span><span class="sxs-lookup"><span data-stu-id="86861-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="86861-203">**ErrorReplacementEnabled**</span><span class="sxs-lookup"><span data-stu-id="86861-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-204">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-206">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar" ) </span><span class="sxs-lookup"><span data-stu-id="86861-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="86861-207">若 **為 TRUE**，則會以 **ErrorReplaceCharacter** 值取代以同位錯誤接收的位元組。</span><span class="sxs-lookup"><span data-stu-id="86861-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="86861-208">只有當此屬性為 **TRUE** 且已啟用同位時，才會取代具有同位錯誤的字元。</span><span class="sxs-lookup"><span data-stu-id="86861-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="86861-209">**EventCharacter**</span><span class="sxs-lookup"><span data-stu-id="86861-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-210">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-212">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar" ) </span><span class="sxs-lookup"><span data-stu-id="86861-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="86861-213">用來通知事件的控制字元值，例如檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="86861-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="86861-214">範例： ^ e</span><span class="sxs-lookup"><span data-stu-id="86861-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="86861-215">**System.componentmodel.backgroundworker.isbusy**</span><span class="sxs-lookup"><span data-stu-id="86861-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-216">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-218">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 函數 \| CreateFile" ) </span><span class="sxs-lookup"><span data-stu-id="86861-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="86861-219">若 **為 TRUE**，則表示序列埠忙碌中。</span><span class="sxs-lookup"><span data-stu-id="86861-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="86861-220">**名稱**</span><span class="sxs-lookup"><span data-stu-id="86861-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-223">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DeviceMap \\ \\ SerialComm" ) </span><span class="sxs-lookup"><span data-stu-id="86861-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="86861-224">Windows 序列埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="86861-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="86861-225">範例： "COM1"</span><span class="sxs-lookup"><span data-stu-id="86861-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="86861-226">**Parity**</span><span class="sxs-lookup"><span data-stu-id="86861-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-229">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)同位 \| " ) </span><span class="sxs-lookup"><span data-stu-id="86861-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="86861-230">要使用的同位檢查方法。</span><span class="sxs-lookup"><span data-stu-id="86861-230">Method of parity checking to be used.</span></span> <span data-ttu-id="86861-231">同位是做為錯誤檢查技術，其中每個資料單位都包含額外的同位位。</span><span class="sxs-lookup"><span data-stu-id="86861-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="86861-232">然後接收者可以藉由計算已設定的位來確認資料的有效性。</span><span class="sxs-lookup"><span data-stu-id="86861-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="86861-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** ( 「無」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="86861-234">未使用同位檢查。</span><span class="sxs-lookup"><span data-stu-id="86861-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="86861-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**奇數** ( 「奇數」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="86861-236">設定同位檢查位元，以便位元集計數為奇數。</span><span class="sxs-lookup"><span data-stu-id="86861-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="86861-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**甚至** ( 「偶數」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="86861-238">設定同位檢查位元，以便位元集計數為偶數。</span><span class="sxs-lookup"><span data-stu-id="86861-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="86861-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**標記** ( "mark" ) </span><span class="sxs-lookup"><span data-stu-id="86861-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="86861-240">將同位檢查位元集保持為 1。</span><span class="sxs-lookup"><span data-stu-id="86861-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="86861-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**空間** ( 「空間」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="86861-242">將同位位設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="86861-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="86861-243">**ParityCheckEnabled**</span><span class="sxs-lookup"><span data-stu-id="86861-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-244">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="86861-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86861-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-246">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity" ) </span><span class="sxs-lookup"><span data-stu-id="86861-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="86861-247">若 **為 TRUE**，則會啟用同位檢查。</span><span class="sxs-lookup"><span data-stu-id="86861-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="86861-248">**RTSFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="86861-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86861-251">要求傳送 (RTS) 流量控制。</span><span class="sxs-lookup"><span data-stu-id="86861-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="86861-252">使用 RTS 來指示資料可供傳輸。</span><span class="sxs-lookup"><span data-stu-id="86861-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="86861-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**啟用** ( "enable" ) </span><span class="sxs-lookup"><span data-stu-id="86861-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="86861-254">資料傳輸會話的 RTS 會保持開啟。</span><span class="sxs-lookup"><span data-stu-id="86861-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="86861-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 ( 「停用」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="86861-256">收到第一個 RTS 信號之後，會忽略 RTS。</span><span class="sxs-lookup"><span data-stu-id="86861-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="86861-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**交握** ( 「交握」 ) </span><span class="sxs-lookup"><span data-stu-id="86861-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="86861-258">如果傳輸緩衝區超過三個季滿，則會關閉 RTS，而且當緩衝區小於一半時，會開啟 rts。</span><span class="sxs-lookup"><span data-stu-id="86861-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="86861-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**切換** ( "切換" ) </span><span class="sxs-lookup"><span data-stu-id="86861-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="86861-260">如果有任何資料緩衝處理以進行傳輸，則會開啟 RTS。</span><span class="sxs-lookup"><span data-stu-id="86861-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="86861-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="86861-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-262">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-264">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="86861-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="86861-265">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="86861-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="86861-266">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="86861-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="86861-267">**StopBits**</span><span class="sxs-lookup"><span data-stu-id="86861-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86861-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86861-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-270">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits" ) </span><span class="sxs-lookup"><span data-stu-id="86861-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="86861-271">要使用的停止位數目。</span><span class="sxs-lookup"><span data-stu-id="86861-271">Number of stop bits to be used.</span></span> <span data-ttu-id="86861-272">停止位會將非同步序列連接上的每個資料單位分開。</span><span class="sxs-lookup"><span data-stu-id="86861-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="86861-273">當沒有資料可供傳輸時，也會持續傳送這些資料。</span><span class="sxs-lookup"><span data-stu-id="86861-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="86861-274">**1** ( "1" ) </span><span class="sxs-lookup"><span data-stu-id="86861-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="86861-275">**1.5** ( "1.5" ) </span><span class="sxs-lookup"><span data-stu-id="86861-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="86861-276">**2** ( "2" ) </span><span class="sxs-lookup"><span data-stu-id="86861-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86861-277">**XOffCharacter**</span><span class="sxs-lookup"><span data-stu-id="86861-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-278">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-280">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar" ) </span><span class="sxs-lookup"><span data-stu-id="86861-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="86861-281">傳輸和接收的 XOFF 字元值。</span><span class="sxs-lookup"><span data-stu-id="86861-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="86861-282">XOFF 是用來停止傳輸資料 (的軟體控制項，而 RTS 和 CTS 則是) 的硬體控制項。</span><span class="sxs-lookup"><span data-stu-id="86861-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="86861-283">XON 會繼續傳輸。</span><span class="sxs-lookup"><span data-stu-id="86861-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="86861-284">**XOffXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="86861-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-287">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim" ) </span><span class="sxs-lookup"><span data-stu-id="86861-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="86861-288">傳送 XOFF 字元之前，輸入緩衝區中允許的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="86861-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="86861-289">**XOnCharacter**</span><span class="sxs-lookup"><span data-stu-id="86861-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-290">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-292">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar" ) </span><span class="sxs-lookup"><span data-stu-id="86861-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="86861-293">用於傳輸和接收的 XON 字元值。</span><span class="sxs-lookup"><span data-stu-id="86861-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="86861-294">XON 是一種軟體控制，可繼續傳輸資料 (而 RTS 和 CTS 則是) 的硬體控制項。</span><span class="sxs-lookup"><span data-stu-id="86861-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="86861-295">XOFF 停止傳輸。</span><span class="sxs-lookup"><span data-stu-id="86861-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="86861-296">**XOnXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="86861-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-297">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-299">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim" ) </span><span class="sxs-lookup"><span data-stu-id="86861-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="86861-300">傳送 XON 字元之前，輸入緩衝區中允許的位元組數目下限。</span><span class="sxs-lookup"><span data-stu-id="86861-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="86861-301">這個屬性會與 **XOffXMitThreshold** 搭配使用，以管制傳輸資料的速率。</span><span class="sxs-lookup"><span data-stu-id="86861-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="86861-302">**XOnXOffInFlowControl**</span><span class="sxs-lookup"><span data-stu-id="86861-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-303">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-305">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX" ) </span><span class="sxs-lookup"><span data-stu-id="86861-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="86861-306">若 **為 TRUE**，則會在接收期間使用 XON/XOFF 流量控制。</span><span class="sxs-lookup"><span data-stu-id="86861-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="86861-307">若 **為 TRUE**，當輸入緩衝區進入已滿的 **XOffXMitThreshold** 位元組內時，便會傳送 **XOffCharacter** 值，而且當輸入緩衝區進入空的 **XOnXMitThreshold** 位元組內時，便會傳送 **XOnCharacter** 值。</span><span class="sxs-lookup"><span data-stu-id="86861-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="86861-308"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="86861-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="86861-309">FALSE</span><span class="sxs-lookup"><span data-stu-id="86861-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="86861-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="86861-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="86861-311">true</span><span class="sxs-lookup"><span data-stu-id="86861-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="86861-312">**XOnXOffOutFlowControl**</span><span class="sxs-lookup"><span data-stu-id="86861-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86861-313">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="86861-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="86861-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86861-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86861-315">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX" ) </span><span class="sxs-lookup"><span data-stu-id="86861-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="86861-316">**XOnXOffOutFlowControl** 會指定是否在傳輸期間使用 XON 或 XOFF 流量控制。</span><span class="sxs-lookup"><span data-stu-id="86861-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="86861-317">若 **為 TRUE**，則傳輸會在收到 **XOffCharacter** 值時停止，並在收到 **XOnCharacter** 值時重新開機。</span><span class="sxs-lookup"><span data-stu-id="86861-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86861-318">備註</span><span class="sxs-lookup"><span data-stu-id="86861-318">Remarks</span></span>

<span data-ttu-id="86861-319">**Win32 \_ SerialPortConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="86861-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86861-320">規格需求</span><span class="sxs-lookup"><span data-stu-id="86861-320">Requirements</span></span>



| <span data-ttu-id="86861-321">需求</span><span class="sxs-lookup"><span data-stu-id="86861-321">Requirement</span></span> | <span data-ttu-id="86861-322">值</span><span class="sxs-lookup"><span data-stu-id="86861-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86861-323">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86861-323">Minimum supported client</span></span><br/> | <span data-ttu-id="86861-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86861-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86861-325">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86861-325">Minimum supported server</span></span><br/> | <span data-ttu-id="86861-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86861-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86861-327">命名空間</span><span class="sxs-lookup"><span data-stu-id="86861-327">Namespace</span></span><br/>                | <span data-ttu-id="86861-328">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="86861-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86861-329">MOF</span><span class="sxs-lookup"><span data-stu-id="86861-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86861-330"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="86861-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86861-331">DLL</span><span class="sxs-lookup"><span data-stu-id="86861-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86861-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86861-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86861-333">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86861-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86861-334">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="86861-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="86861-335">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="86861-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

---
title: Win32_WinSAT 類別
description: 定義最新正式評量的摘要評估資訊。
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT 類別 WinSAT
- Win32_WinSAT 類別 WinSAT，描述
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a9e863bd22cebc6609e32521b85de4bca29ae048d9673e3b09cfff2b95408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504528"
---
# <a name="win32_winsat-class"></a>Win32 \_ WinSAT 類別

\[**Win32 \_** 在 Windows 8.1 之後，可能會變更或無法使用 WinSAT。\]

定義最新正式評量的摘要評估資訊。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>成員

**Win32 \_ WinSAT** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ WinSAT** 類別具有這些屬性。

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦上的處理器分數。

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在 Windows 8.1 之後，WinSAT 就不會再評估三維圖形 (電腦的遊戲) 功能，以及圖形驅動程式使用此評量轉譯物件和執行著色器的能力。 為了提供相容性，WinSAT 會報告計量和分數的 sentinel 值，但不會即時計算這些值。

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦上主要硬碟的連續讀取輸送量分數。

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦圖形功能的分數。

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦的記憶體輸送量和容量分數。

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

在 WQL 查詢的 WHERE 子句中，這個屬性必須設定為 "MostRecentAssessment"。

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

評量的狀態。 如需可能值的描述，請參閱 [**WINSAT \_ 評定 \_ 狀態**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) 列舉。

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0) 
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**有效** (1) 
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2) 
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3) 
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**無效** 的 (4) 
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦的基本分數。 如需分數值的詳細資訊，請參閱 [**IProvideWinSATResultsInfo：： SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) 屬性。

</dd> </dl>

## <a name="remarks"></a>備註

如需子元件分數（例如 **MemoryScore**）的詳細資訊，請參閱 [**IProvideWinSATAssessmentInfo：：計分**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) 屬性。

## <a name="examples"></a>範例

如需示範如何使用 WMI 從這個類別取出資料的範例，請參閱 [**IProvideWinSATVisuals：： get \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 






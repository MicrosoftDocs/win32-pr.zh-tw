---
title: 'WINBIO_EXTENDED_ENROLLMENT_STATUS 結構 (Winbio \_ 類型 .h) '
description: 包含正在進行中之註冊狀態的其他相關資訊。
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_ENROLLMENT_STATUS 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094063"
---
# <a name="winbio_extended_enrollment_status-structure"></a>WINBIO \_ 延伸 \_ 註冊 \_ 狀態結構

包含正在進行中之註冊狀態的其他相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**TemplateStatus**
</dt> <dd>

註冊範本的範例集合狀態。 此成員可能的值如下。



| 值                                                                                                                                                                                                  | 意義                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ 確定**</dt> </dl>                                                                     | 註冊可供儲存。<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ 不正確作業 \_**</dt> </dl> | 沒有任何註冊正在進行中。<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ 我 \_ 更多 \_ 資料**</dt> </dl>                         | 需要更多範例才能完成範本。<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ 電子 \_ 錯誤 \_ 捕捉**</dt> </dl>                   | 無法使用最新的範例。<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

如果 **templatestatus.archived** 成員的值是 **WINBIO \_ E \_ 錯誤的 \_ 捕獲**，則為最新範例無法使用的原因。

</dd> <dt>

**PercentComplete**
</dt> <dd>

從引擎介面卡取得完成範本百分比的最佳估計值，以0到100的值表示。

</dd> <dt>

**因素**
</dt> <dd>

此結構包含引擎介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。 例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**，則 [**WINBIO \_ 擴充 \_ 引擎 \_ 資訊**](winbio-extended-engine-info.md) 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。

</dd> <dt>

**SubFactor**
</dt> <dd>

**WINBIO \_ 生物識別 \_ 子類型** 值，提供註冊的其他相關資訊。

</dd> <dt>

**特定**
</dt> <dd>

針對特定生物特徵辨識因素進行中之註冊的狀態相關資訊。

<dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**FacialFeatures**
</dt> <dd>

臉部特徵進行中之註冊狀態的相關資訊。

<dl> <dt>

**BoundingBox**
</dt> <dd>

要註冊之個人臉部的相機框架內的位置（以圖元為單位）。 相機框架的大小會決定這個位置的圖元數上限。 取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。 使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。

</dd> <dt>

**距離**
</dt> <dd>

臉部的實際位置與臉部的理想焦距之間的距離。 此值範圍從-100 到100。 0表示理想的距離，正值表示臉部的實際位置太遠，負值表示實際位置太近。

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

針對指紋模式進行中之註冊狀態的相關資訊。

<dl> <dt>

**GeneralSamples**
</dt> <dd>

建立新指紋範本所需的樣本總數。

</dd> <dt>

**中心**
</dt> <dd>

建立新的指紋範本時所需的指紋中心樣本數。

</dd> <dt>

**TopEdge**
</dt> <dd>

建立新的指紋範本所需之指紋上邊緣的樣本數。

</dd> <dt>

**BottomEdge**
</dt> <dd>

建立新的指紋範本所需之指紋下邊緣的樣本數。

</dd> <dt>

**LeftEdge**
</dt> <dd>

建立新的指紋範本所需之指紋左邊緣的樣本數。

</dd> <dt>

**RightEdge**
</dt> <dd>

建立新的指紋範本時所需的指紋右邊的樣本數。

</dd> </dl> </dd> <dt>

**虹膜**
</dt> <dd>

鳶尾花模式進行中之註冊狀態的相關資訊。

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。 如果鳶尾花辨識系統只監視一眼，這個位置就是該眼睛的鳶尾花。 如果鳶尾花辨識系統同時監視這兩眼，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛鳶尾花。 如果鳶尾花辨識系統同時監視這兩個眼睛，而兩個眼睛都在攝影機框架中，則這個位置可能是個人的正確眼睛鳶尾花。

相機框架的大小會決定這個位置的圖元數上限。 取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。 使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。 如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。 如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的最左邊鳶尾花。

相機框架的大小會決定這個位置的圖元數上限。 取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。 使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

要註冊之個人的其中一個瞳孔中心位置。 如果鳶尾花辨識系統只監控一眼，這個位置就是該眼睛小學生的中心。 如果鳶尾花辨識系統同時監視這兩種情況，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛小學生中心。 如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的適當眼睛小學生中心。

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

要註冊之個人的其中一個瞳孔中心位置。 如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。 如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人左側的小學生中心。

</dd> <dt>

**距離**
</dt> <dd>

鳶尾花的實際位置與鳶尾花的理想焦距距離之間的距離。 此值範圍從-100 到100。 0表示理想的距離，正值表示鳶尾花的實際位置太遠，負值則表示實際位置太近。

</dd> </dl> </dd> <dt>

**語音**
</dt> <dd>

語音模式進行中的註冊狀態相關資訊。

<dl> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



 

 






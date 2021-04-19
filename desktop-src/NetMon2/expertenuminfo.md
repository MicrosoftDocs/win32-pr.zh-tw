---
description: EXPERTENUMINFO 結構提供專家的相關資訊。
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: 'EXPERTENUMINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972815"
---
# <a name="expertenuminfo-structure"></a>EXPERTENUMINFO 結構

**EXPERTENUMINFO** 結構提供專家的相關資訊。 網路監視器會為結構配置記憶體，並在呼叫 [**註冊專家**](register-expert.md) 函式時將它傳遞給專家。 當專家收到結構時，就必須填寫網路監視器要求的所有資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**szName**
</dt> <dd>

專家的名稱。

</dd> <dt>

**szVendor**
</dt> <dd>

建立專家的廠商名稱。

</dd> <dt>

**szDescription**
</dt> <dd>

專家的描述。 **SzDescription** 成員的值可能是 **Null**。 如果名稱太長，則會在預設檢視器設定中被截斷。

</dd> <dt>

**版本**
</dt> <dd>

此值必須為零。

</dd> <dt>

**旗標**
</dt> <dd>

下列旗標描述專家。



| 值                                                                                                                                                                                                                                                    | 意義                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**可設定專家 \_ 列舉 \_ 旗標 \_**</dt> </dl>                                          | 專家支援對 [**Configure**](configure.md) 方法的呼叫。 <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**私用的專家 \_ 列舉 \_ 旗標 \_ 檢視器 \_**</dt> </dl>                                   | 專家需要私人 (非共用) 事件檢視器。 <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**專家 \_ 列舉 \_ 旗標 \_ 沒有 \_ 檢視器**</dt> </dl>                                                  | 專家不會傳送事件通知。 <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**專家 \_ 列舉 \_ 旗標 \_ 將 \_ 我新增 \_ 至 \_ RMC \_ \_ 摘要**</dt> </dl> | 當焦點在 [摘要] 窗格中時，專家會出現在內容功能表上。 <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**專家 \_ 列舉 \_ 旗標更 \_ 詳細地將 \_ 我新增 \_ 至 \_ RMC \_ \_**</dt> </dl>    | 當焦點在 [詳細資料] 窗格中時，專家會出現在內容功能表上。 <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

專家的控點。 使用 **EXPERTENUMINFO** 結構來註冊專家時，會忽略參數。

</dd> <dt>

**szDllName**
</dt> <dd>

私用成員;請勿使用。

</dd> <dt>

**hModule**
</dt> <dd>

私用成員;請勿使用。

</dd> <dt>

**pRegisterProc**
</dt> <dd>

私用成員;請勿使用。

</dd> <dt>

**pConfigProc**
</dt> <dd>

私用成員;請勿使用。

</dd> <dt>

**pRunProc**
</dt> <dd>

私用成員;請勿使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 





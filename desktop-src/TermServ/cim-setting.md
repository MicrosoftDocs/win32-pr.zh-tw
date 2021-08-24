---
title: 'CIM_Setting 類別 (遠端桌面服務) '
description: 代表一或多個 managed 系統元素的設定相關和指令引數。
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- CIM_Setting 類別遠端桌面服務
- CIM_Setting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53499c383c6fcf9ae2774427afcea2ea339408ff0292a3d4ce15286a4a75298
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131317"
---
# <a name="cim_setting-class-remote-desktop-services"></a>CIM_Setting 類別 (遠端桌面服務) 

代表一或多個 managed 系統元素的設定相關和指令引數。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a>成員

**CIM \_ 設定** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ 設定** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

簡短描述 (物件的單行字串) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") 
</dt> </dl>

物件的安裝日期。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

<dt>



  ( [確定] ) 


</dt> <dd></dd> <dt>



  ( 「錯誤」 ) 


</dt> <dd></dd> <dt>



  ( 「降級」 ) 


</dt> <dd></dd> <dt>



  ( 「未知」 ) 


</dt> <dd></dd> <dt>



  ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>



  ( 「開始」 ) 


</dt> <dd></dd> <dt>



  ( 「正在停止」 ) 


</dt> <dd></dd> <dt>



  ( "Service" ) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> </dl>

 


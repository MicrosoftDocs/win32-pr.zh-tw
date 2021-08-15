---
title: MSAD_DomainController 類別
description: 代表執行 WMI 提供者的網域控制站 (DC) 。
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController 類別 Active Directory
- MSAD_DomainController 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a428d1c852d93fb34bfc3188219bd8ffdc5020ae65c5f9191c44d075b603a143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186083"
---
# <a name="msad_domaincontroller-class"></a>MSAD 的 [ \_ 控制器] 類別

代表執行 WMI 提供者的網域控制站 (DC) 。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>成員

MSAD 的 [ **\_ 控制器** ] 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

MSAD 的 [ **\_ 控制器** ] 類別具有這些方法。



| 方法                                                 | 描述                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | 叫用知識一致性檢查程式，以確認複寫拓撲。<br/> |



 

### <a name="properties"></a>屬性

MSAD 的 [ **\_ 控制器** ] 類別具有這些屬性。

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得伺服器物件的一般名稱。

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得 [**NTDS DSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件的 X. 500 路徑。

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出 DC 上的定位器服務是否正確地廣告。 如果 DC 上的定位器服務正確通告，則 **為 TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出 DC 是否為通用類別目錄伺服器。 如果 DC 是通用類別目錄伺服器，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出 DC 是否已取得另一個 RID 集區。 **如果 DC** 已取得另一個 RID 集區，而且即使目前的 rid 集區已用盡，此 dc 上的 rid 的配置仍可繼續。否則 **為 FALSE**。

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 DNS 中正確註冊 DC。 如果 DC 已在 DNS 中正確註冊，則 **為 TRUE** 。否則 **為 FALSE**。

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出 SysVol 是否已正確發佈。 如果 SysVol 已正確發行，則 **為 TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得與設定容器中的 [**NTDS DSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件相關聯的 GUID。 **NTDS DSA** 物件代表伺服器上的 ACTIVE DIRECTORY 網域 Service DSA 進程。

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得保留在此 DC 上目前 RID 集區中的 Rid 百分比。

</dd> <dt>

**SiteName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得 DC 所在的網站。

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得仍在此網域控制站上的佇列中最舊的複寫新增作業的時間戳記。

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得仍在此網域控制站上的佇列中之最舊複寫刪除作業的時間戳記。

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得在此網域控制站上仍在佇列中之最舊複寫修改作業的時間戳記。

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得仍在此網域控制站上的佇列中最舊複寫同步作業的時間戳記。

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得仍在此網域控制站上的佇列中之最舊複寫更新作業的時間戳記。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 


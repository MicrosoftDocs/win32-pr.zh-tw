---
title: Win32_RDMSJoinedNode 類別
description: 代表由遠端桌面管理服務 (RDMS) 管理的伺服器節點。
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode 類別遠端桌面服務
- Win32_RDMSJoinedNode 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383962"
---
# <a name="win32_rdmsjoinednode-class"></a>Win32 \_ RDMSJoinedNode 類別

代表由遠端桌面管理服務 (RDMS) 管理的伺服器節點。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a>成員

**Win32 \_ RDMSJoinedNode** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ RDMSJoinedNode** 類別具有這些方法。



| 方法                                                                | 描述                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetJoinedNodeCount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows server 2012 R2 和 Windows server 2012：** 此方法在 Windows Server 2016 之前無法使用。<br/> 取得已安裝指定角色的伺服器數目。<br/> |
| [**加入**](join-win32-rdmsjoinednode.md)                             | 將節點新增至 RDM。<br/>                                                                                                                                                                       |
| [**退出**](unjoin-win32-rdmsjoinednode.md)                         | 從 RDM 移除節點。<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>屬性

**Win32 \_ RDMSJoinedNode** 類別具有這些屬性。

<dl> <dt>

**FQDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

取得節點的完整功能變數名稱。

</dd> <dt>

**IsGatewayCertificateInstalled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否具有憑證，可執行遠端桌面閘道連線的驗證。 如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsPublishingCertificateInstalled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否具有憑證來簽署遠端桌面通訊協定發行檔案。 如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRdcb**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否為遠端桌面連線代理人。 如果伺服器是遠端桌面連線代理人，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRdg**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否為遠端桌面閘道伺服器。 如果伺服器是遠端桌面閘道伺服器，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRdls**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否為遠端桌面授權伺服器。 如果伺服器是遠端桌面授權伺服器，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRdsh**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否為遠端桌面工作階段主機伺服器。 如果伺服器是遠端桌面工作階段主機伺服器，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRdvh**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否為遠端桌面虛擬化主機。 如果伺服器是遠端桌面虛擬化主機，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRdwa**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否為遠端桌面 web 存取伺服器。 如果伺服器是遠端桌面 Web 存取伺服器，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsRedirectorCertificateInstalled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否具有憑證來執行遠端桌面服務部署的驗證。 如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsWebAccessCertificateInstalled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定值，這個值會指出伺服器是否具有憑證，可執行遠端桌面 Web 存取的驗證。 如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

取得和設定節點上的作業系統版本。

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

取得節點 (SID) 的安全識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面管理服務提供者](rdms-api-reference.md)
</dt> </dl>

 


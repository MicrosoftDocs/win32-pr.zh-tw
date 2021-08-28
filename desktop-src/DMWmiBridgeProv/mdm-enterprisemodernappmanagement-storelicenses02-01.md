---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別
description: MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 類別可用來管理 store 應用程式的授權。
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0342acc9cb74825552a409d686e5bc55f0cebc75642d5981a7144f3bac74bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018106"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a>MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別可用來管理 store 應用程式的授權。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a>成員

**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別具有這些方法。



| 方法                                                                                                              | 描述                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**AddLicenseMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | 新增授權的方法。<br/>                 |
| [**GetLicenseFromStoreMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | 從存放區取得授權的方法。<br/> |



 

### <a name="properties"></a>屬性

**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

選擇性節點。 存放區已安裝應用程式的授權識別碼。 授權識別碼通常是應用程式的 PFN。

支援的作業為 [新增]、[取得] 和 [刪除]。

</dd> <dt>

[LicenseCategory](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[LicenseUsage](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"

</dd> <dt>

[RequesterID](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


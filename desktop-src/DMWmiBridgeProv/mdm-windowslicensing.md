---
title: MDM_WindowsLicensing 類別
description: MDM \_ WindowsLicensing 類別是針對授權相關的管理案例所設計。
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9470b72cb6a50323af9294be4a6506682fc7aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480924"
---
# <a name="mdm_windowslicensing-class"></a>MDM \_ WindowsLicensing 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ WindowsLicensing** 類別是針對授權相關的管理案例所設計。 目前的範圍僅限於 Windows 10 桌面和行動裝置的版本升級，例如 Windows 10 企業版的 Windows 10 專業版。 此外，此 CSP 也提供啟用或變更 Windows 10 桌面裝置之產品金鑰的功能。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a>成員

**MDM \_ WindowsLicensing** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MDM \_ WindowsLicensing** 類別具有這些方法。




| 方法 | 描述 | 
|--------|-------------|
| <a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a> | 安裝 Windows 10 桌面裝置的產品金鑰。 不會重新開機。<br /> | 
| <a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a> | 方法，檢查輸入的產品金鑰是否可用於版本升級、啟用或變更桌面裝置 Windows 10 的產品金鑰。<br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a> | 針對 Windows 10 行動裝置的版本升級提供授權。<br /><blockquote>[!Note]<br />此升級程式不需要重新開機系統。</blockquote><br /><br /> 日期類型是 XML。<br /> 支援的作業為執行。<br /><blockquote>[!Important]<br />XML 授權檔案內容必須經過正確的轉義 (也就是說，它不應該只是複製的 XML) ，否則 Windows 10 行動裝置上的版本升級將會失敗。 如需有關 XML 授權檔案正確地轉義的詳細資訊，請參閱 <a href="https://www.w3.org/TR/xml/">W3C XML 規格</a>的2.4 節。XML 授權檔案是從 Microsoft 大量授權服務中心取得的。 您的組織必須具有 Microsoft 的大量授權合約，才能存取入口網站。</blockquote><br /> 以下是透過 MDM 或布建套件使用此節點時的有效版本升級路徑：<ul><li>Windows 10Mobileto Windows 10 行動裝置企業版<br /></li></ul><br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a> | 觸發裝置以取得產品金鑰，並升級用戶端的版本。<blockquote>[!Note]<br />此升級程式需要重新開機系統。</blockquote><br /><br /> 支援的作業為執行。<br /> 將產品金鑰從 MDM 伺服器推送到使用者的裝置時， <strong>changepk.exe</strong> 使用產品金鑰執行。 完成之後，就會向使用者顯示通知，指出有新版本的 Windows 10 可供使用。 然後，使用者可以手動重新開機其系統，或在兩個小時之後，自動重新開機裝置以完成升級。 使用者會在自動重新開機前10分鐘收到提醒通知。<br /> 裝置重新啟動之後，版本升級程序便完成。 使用者將會收到成功升級的通知。<blockquote>[!Important]<br />如果另一個原則需要在執行 <strong>changepk.exe</strong> 時發生系統重新開機，則版本升級將會失敗。</blockquote><br /><br /> 如果在佈建套件中輸入產品金鑰，而且使用者開始安裝套件，會向使用者顯示通知，告知他們的系統會重新啟動才能完成套件安裝。 明確同意使用者進行時，套件會繼續安裝，並使用產品金鑰 <strong>changepk.exe</strong> 執行。 自動重新開機之前使用者將會收到提醒通知 30 秒。 <br /> 裝置重新啟動之後，版本升級程序便完成。 使用者將會收到成功升級的通知。 <br /> 此節點也可用來在特定版本的 Windows 10 桌面裝置上，藉由輸入產品金鑰來啟用或變更產品金鑰。 啟用或變更產品金鑰不需要重新開機，而且是使用者的無訊息處理常式。<br /><blockquote>[!Important]<br />輸入的產品金鑰必須是29個字元 (也就是說，它應該包含連字號) ，否則 Windows 10 桌面裝置上的啟用、版本升級或產品金鑰變更將會失敗。 從 Microsoft 大量授權服務中心取得產品金鑰。 您的組織必須具有 Microsoft 的大量授權合約，才能存取入口網站。</blockquote><br /> 以下是透過 MDM 使用此節點時的有效版本升級路徑：<ul><li>Windows 10 企業版至 Windows 10 教育版</li><li>Windows 10 家用版至 Windows 10 教育版</li><li>Windows 10 專業版至 Windows 10 教育版</li><li>Windows 10 專業版至 Windows 10 企業版</li></ul><br /> 您可以在下列版本上執行啟用或變更產品金鑰：<ul><li>Windows 10 Education</li><li>Windows 10 Enterprise</li><li>Windows 10 Home</li><li>Windows 10 Pro</li></ul><br /> | 




 

### <a name="properties"></a>屬性

**MDM \_ WindowsLicensing** 類別具有這些屬性。

<dl> <dt>

[版本(Edition)](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
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

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/"

</dd> <dt>

[狀態](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


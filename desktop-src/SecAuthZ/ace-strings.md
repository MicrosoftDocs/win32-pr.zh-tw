---
description: 說明在存取控制專案中使用的字串。
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: ACE 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60e8f4f5d3cd94f6e871b3b4962d2d548afa003c3bd4aa37a1ae8f008ce1a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785399"
---
# <a name="ace-strings"></a>ACE 字串

[安全描述項定義語言](security-descriptor-definition-language.md) (SDDL) 在 [*安全描述項*](/windows/desktop/SecGloss/s-gly)字串的 DACL 和 SACL 元件中使用 ACE 字串。

如 [安全描述項字串格式](security-descriptor-string-format.md) 範例所示，安全描述項字串中的每個 ACE 都會以括弧括住。 ACE 的欄位會以下列順序排列，並以分號分隔 (; ) 。

> [!Note]  
> 條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 的格式與其他 ace 類型 (ace) 不同。 針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>欄位

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**ace \_ 類型**
</dt> <dd>

字串，指出 [**ACE \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header)結構之 **AceType** 成員的值。 ACE 類型字串可以是在 Sddl 中定義的下列其中一個字串。



| ACE 類型字串 | Sddl 中的常數                      | AceType 值                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "A"             | \_允許 SDDL 存取 \_                   | 存取 \_ 允許的 \_ ACE \_ 類型                                                                                                                                         |
| "D"             | SDDL \_ \_ 拒絕存取                    | \_拒絕存取 \_ ACE \_ 類型                                                                                                                                          |
| OA            | \_允許 SDDL 物件 \_ 存取 \_           | 存取 \_ 允許的 \_ 物件 \_ ACE \_ 類型                                                                                                                                 |
| OD            | SDDL \_ 物件 \_ \_ 拒絕存取            | \_拒絕存取 \_ 物件 \_ ACE \_ 類型                                                                                                                                  |
| 澳大利亞            | SDDL \_ 審核                             | 系統 \_ 審核 \_ ACE \_ 類型                                                                                                                                           |
| "AL"            | SDDL \_ 警示                             | 系統 \_ 警示 \_ ACE \_ 類型                                                                                                                                           |
| /OU            | SDDL \_ 物件 \_ AUDIT                     | SYSTEM \_ AUDIT \_ OBJECT \_ ACE \_ 類型                                                                                                                                   |
| 歐            | SDDL \_ 物件 \_ 警示                     | 系統 \_ 警報 \_ 物件 \_ ACE \_ 類型                                                                                                                                   |
| "ML"            | SDDL \_ 強制 \_ 標籤                  | 系統 \_ 強制 \_ 標籤 \_ ACE \_ 類型 **Windows Server 2003：** 無法使用。                                                                                        |
| XA            | \_允許 SDDL 回呼 \_ 存取 \_         | 存取 \_ 允許的 \_ 回呼 \_ ACE \_ 類型 **Windows Server 2008、Windows Vista 和 Windows server 2003：** 無法使用。                                                |
| XD            | SDDL \_ 回呼 \_ \_ 拒絕存取          | \_拒絕存取 \_ 回呼 \_ ACE \_ 類型 **Windows Server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                                                 |
| RA            | SDDL \_ 資源 \_ 屬性               | 系統 \_ 資源 \_ 屬性 \_ ACE \_ 類型 **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。<br/> |
| SP-1            | SDDL \_ 範圍 \_ 原則 \_ 識別碼                | 系統 \_ 範圍 \_ 原則 \_ 識別碼 \_ ACE \_ 類型 **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。<br/>  |
| XU            | SDDL \_ 回呼 \_ 審核                   | 系統 \_ AUDIT \_ 回呼 \_ ACE \_ 類型 **Windows Server 2008 R2、Windows 7、Windows Server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。<br/>     |
| ZA            | \_允許 SDDL 回呼 \_ 物件 \_ 存取 \_ | 存取 \_ 允許的 \_ 回呼 \_ ACE \_ 類型 **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。<br/>   |
| TL            | SDDL \_ 進程 \_ 信任 \_ 標籤             | 系統 \_ 進程 \_ 信任 \_ 標籤 \_ ACE \_ 類型 **Windows Server 2012、Windows 8、Windows Server 2008 R2、Windows 7、Windows Server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
| 奧蘭多            | SDDL \_ 存取 \_ 篩選                    | 系統 \_ 存取 \_ 篩選 \_ ACE \_ 類型 **Windows Server 2016、Windows 10 1607 版、Windows 10 1511 版、Windows 10 1507 版、Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
 

> [!Note]  
> 如果 **ace \_ 類型** 為 access \_ 允許 \_ \_ 的物件 ace \_ 類型， **而且物件 \_ guid** 或 **繼承 \_ 物件 \_ guid** 都未指定 [**guid**](/windows/win32/api/guiddef/ns-guiddef-guid) ，則 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 會將 **ace \_ 類型** 轉換成存取允許的 \_ \_ ace \_ 類型。

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace \_ 旗標**
</dt> <dd>

字串，指出 [**ACE \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header)結構之 **AceFlags** 成員的值。 ACE 旗標字串可以是以 Sddl. h 定義的下列字串的串連。



| ACE 旗標字串 | Sddl 中的常數       | AceFlag 值                 |
|------------------|--------------------------|-------------------------------|
| CI             | SDDL \_ 容器 \_ 繼承 | 容器 \_ 繼承 \_ ACE       |
| OI             | SDDL \_ 物件 \_ 繼承    | OBJECT \_ INHERIT \_ ACE          |
| NP-IN             | SDDL \_ 沒有 \_ 傳播      | 沒有 \_ 傳播 \_ 繼承 \_ ACE   |
| IO             | SDDL \_ \_ 只繼承      | \_只繼承 \_ ACE            |
| 「識別碼」             | SDDL \_ 繼承          | 繼承的 \_ ACE                |
| SA             | SDDL \_ 審核 \_ 成功     | 成功的 \_ 存取 \_ ACE \_ 旗標 |
| FA             | SDDL \_ 審核 \_ 失敗     | \_存取 \_ ACE \_ 旗標失敗     |
| TP             | SDDL \_ 信任 \_ 受保護的 \_ 篩選 | 信任 \_ PROTECTED \_ FILTER \_ ACE \_ 旗標 **Windows Server 2016、Windows 10 1607 版、Windows 10 1511 版、Windows 10 1507 版、Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
| CR             | SDDL \_ 重大           | 重大 \_ ACE \_ 旗標 **Windows Server 1803 版、Windows 10 1803 版、Windows Server 1709、Windows 10 1709、Windows 10 version 1703、Windows Server 2016、Windows 10 version 1607、Windows 10 version 1511、Windows 10 version 1507、Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8 Windows Server 2008 R2、Windows 7、Windows伺服器2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**權利**
</dt> <dd>

表示由 ACE 所控制之 [存取權限](access-rights-and-access-masks.md) 的字串。 這個字串可以是存取權限的十六進位字串標記法（例如 "0x7800003F"），也可以是下列字串的串連。



### <a name="generic-access-rights"></a>一般存取權限

| 存取權限字串 | Sddl 中的常數 | 存取權限值 |
|----------------------|--------------------|--------------------|
| 正式                 | SDDL \_ 泛型 \_ 全部 | 一般 \_ 全部       |
| GR                 | SDDL \_ 一般 \_ 讀取 | 一般 \_ 讀取     |
| GW                 | SDDL \_ 一般 \_ 寫入 | 一般 \_ 寫入 |
| GX                 | SDDL \_ 泛型 \_ 執行 | 一般 \_ 執行 |


### <a name="standard-access-rights"></a>標準存取權限

| 存取權限字串 | Sddl 中的常數 | 存取權限值 |
|----------------------|--------------------|--------------------|
| RC                 | SDDL \_ 讀取 \_ 控制 | 讀取 \_ 控制      |
| SD                 | SDDL \_ 標準 \_ 刪除 | DELETE          |
| WD                 | SDDL \_ 寫入 \_ DAC | 寫入 \_ DAC            |
| WO                 | SDDL \_ 寫入 \_ 擁有者 | 寫入 \_ 擁有者        |

### <a name="directory-service-object-access-rights"></a>目錄服務物件存取權限

| 存取權限字串 | Sddl 中的常數 | 存取權限值 |
|----------------------|--------------------|--------------------|
| 開頭                 | SDDL \_ 讀取 \_ 屬性 | ADS \_ 正確的 \_ DS \_ 讀取 \_ |
| WP                 | SDDL \_ 寫入 \_ 屬性 | ADS \_ 正確的 \_ DS \_ 寫入 \_ |
| CC                 | SDDL \_ 建立 \_ 子系 | ADS \_ RIGHT \_ DS \_ 建立 \_ 子系 |
| 電源                 | SDDL \_ 刪除 \_ 子系 | ADS \_ 正確的 \_ DS \_ 刪除 \_ 子系 |
| 小寫                 | SDDL \_ 清單 \_ 子系 | ADS \_ RIGHT \_ ACTRL \_ DS \_ 清單 |
| 接線                 | SDDL \_ 自我 \_ 寫入    | ADS \_ 適合 \_ DS \_ 自助 |
| 高低                  | SDDL \_ 清單 \_ 物件 | ADS \_ 正確的 \_ DS \_ 清單 \_ 物件 |
| 診斷                 | SDDL \_ 刪除 \_ 樹狀目錄 | ADS \_ 正確的 \_ DS \_ 刪除 \_ 樹狀結構 |
| CR                  | SDDL \_ 控制項 \_ 存取 | ADS \_ 正確的 \_ DS \_ 控制 \_ 存取 |

### <a name="file-access-rights"></a>檔案存取權限

| 存取權限字串 | Sddl 中的常數 | 存取權限值 |
|----------------------|--------------------|--------------------|
| FA                 | SDDL \_ 檔案 \_ 全部    | 檔案 \_ 所有 \_ 存取   |
| 法國                 | SDDL \_ 檔案 \_ 讀取   | 檔案 \_ 一般 \_ 讀取 |
| FW                 | SDDL \_ 檔案 \_ 寫入  | 檔案 \_ 一般 \_ 寫入 |
| FX                 | SDDL \_ 檔案 \_ 執行 | FILE \_ GENERIC \_ EXECUTE |


### <a name="registry-key-access-rights"></a>登錄機碼存取權限

| 存取權限字串 | Sddl 中的常數 | 存取權限值 |
|----------------------|--------------------|--------------------|
| KA                 | SDDL \_ 金鑰 \_ 全部     | 金鑰 \_ 所有 \_ 存取權   |
| 南韓                 | SDDL \_ 金鑰 \_ 讀取    | 金鑰 \_ 讀取          |
| 知識                 | SDDL \_ 金鑰 \_ 寫入   | 金鑰 \_ 寫入         |
| "KX"                 | SDDL \_ 金鑰 \_ 執行 | 金鑰 \_ 執行       |

### <a name="mandatory-label-rights"></a>強制標籤許可權

| 存取權限字串 | Sddl 中的常數 | 存取權限值 |
|----------------------|--------------------|--------------------|
| NR                 | SDDL \_ 沒有 \_ 讀取 \_ | 系統 \_ 強制 \_ 卷 \_ 標 \_ 否 \_ 讀取 **Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。 |
| NW                 | SDDL \_ 沒有 \_ 寫入 \_ | 系統 \_ 強制 \_ 卷 \_ 標 \_ 不 \_ 會寫入 **Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。 |
| NX                 | SDDL \_ 沒有 \_ 執行 \_ | 系統 \_ 強制 \_ 卷 \_ 標 \_ 不 \_ 會執行 **Windows Server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**物件 \_ guid**
</dt> <dd>

GUID 的字串標記法，指出物件特定 ACE 結構的 **ObjectType** 成員值，例如 [**存取 \_ 允許的 \_ 物件 \_ ace**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)。 GUID 字串會使用 [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) 函數所傳回的格式。

下表列出一些常用的物件 Guid。



| 許可權和 GUID                         | 權限      |
|-----------------------------------------|-----------------|
| CR; ab721a53-1e2f-11d0-9819-00aa0040529b | 變更密碼 |
| CR; 00299570-246d-11d0-a768-00aa006e0529 | 重設密碼  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**繼承 \_ 物件 \_ guid**
</dt> <dd>

GUID 的字串表示，指出物件特定 ACE 結構的 **InheritedObjectType** 成員值。 GUID 字串使用 [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) 格式。

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**帳戶 \_ sid**
</dt> <dd>

識別 ACE[信任者](trustees.md)的[SID 字串](sid-strings.md)。

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**資源 \_ 屬性**
</dt> <dd>

\[選擇性 \] ：資源 \_ 屬性僅適用于資源 ace，而且是選擇性的。 指出資料類型的字串。 資源屬性 ace 資料類型可以是在 Sddl 中定義的下列其中一種資料類型。

\#在資源屬性中，"" 符號與 "0" 同義。 例如，D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \#) ) 相當於並解釋為 D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 01020300) ) 。

**Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista 和 Windows Server 2003：** 無法使用資源屬性。



| 資源屬性 ace 資料類型字串 | Sddl 中的常數 | 資料類型        |
|-----------------------------------------|--------------------|------------------|
| TI                                    | SDDL \_ INT          | 帶正負號的整數   |
| TU                                    | SDDL \_ UINT         | 不帶正負號的整數 |
| 有毒                                    | SDDL \_ WSTRING      | 寬字元串      |
| T                                    | SDDL \_ SID          | SID              |
| TX                                    | SDDL \_ BLOB         | 八位字串     |
| TB                                    | SDDL \_ 布林值      | Boolean          |



 

</dd> </dl>

下列範例顯示存取允許之 ACE 的 ACE 字串。 它不是物件特定的 ACE，因此它在 **物件 \_ guid** 中沒有任何資訊，而且會 **繼承 \_ 物件 \_ guid** 欄位。 **Ace \_ 旗標** 欄位也是空的，這表示沒有設定任何 ace 旗標。


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



以上顯示的 ACE 字串會描述下列 ACE 資訊。


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



下列範例會顯示以資源宣告分類的檔案，用於 Windows 和結構化查詢語言 (SQL)  (SQL 的密碼設定為高業務影響的) 。


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



以上顯示的 ACE 字串會描述下列 ACE 資訊。


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



如需詳細資訊，請參閱 [安全描述項字串格式](security-descriptor-string-format.md) 和 [SID 字串](sid-strings.md)。 針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>


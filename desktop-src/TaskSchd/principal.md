---
title: Principal 物件
description: 提供主體安全性認證的腳本物件。
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Principal 物件工作排程器
- 主體物件工作排程器，說明
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843324"
---
# <a name="principal-object"></a>Principal 物件

提供主體安全性認證的腳本物件。 這些安全性認證會定義與主體相關聯之工作的安全性內容。

## <a name="members"></a>成員

**Principal** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Principal** 物件具有這些屬性。



| 屬性                                                | 存取類型           | Description                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | 讀取/寫入<br/> | 取得或設定工作排程器 UI 中顯示之主體的名稱。<br/>                                                                |
| [**GroupId**](principal-groupid.md)<br/>         | 讀取/寫入<br/> | 取得或設定執行與主體相關聯之工作所需之使用者群組的識別碼。<br/>                           |
| [**Id**](principal-id.md)<br/>                   | 讀取/寫入<br/> | 取得或設定主體的識別碼。<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | 讀取/寫入<br/> | 取得或設定執行與主體相關聯之工作所需的安全性登入方法。<br/>                                  |
| [**RunLevel**](principal-runlevel.md)<br/>       | 讀取/寫入<br/> | 取得或設定識別碼，這個識別碼用來指定執行與主體相關聯之工作所需的許可權層級。<br/> |
| [**UserId**](principal-userid.md)<br/>           | 讀取/寫入<br/> | 取得或設定執行與主體相關聯之工作所需的使用者識別碼。<br/>                                        |



 

## <a name="remarks"></a>備註

指定帳戶時，請記得在程式碼中正確使用雙反斜線來指定網域和使用者名稱。 例如，使用網域 \\ \\ 使用者名稱來指定 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid)屬性的值。

讀取或寫入工作的 XML 時，主體的安全性認證是在工作排程器架構的 [**principal**](taskschedulerschema-principal-principaltype-element.md) 元素中指定。

如果工作是使用 at.exe 命令列工具來註冊，而且此物件是用來取得工作的相關資訊，則 [**LogonType**](principal-logontype.md) 屬性會傳回0， [**RunLevel**](principal-runlevel.md) 屬性將會傳回0，而且 [**UserId**](principal-userid.md) 屬性不會傳回任何內容。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






---
title: RegistrationInfo. 作者屬性
description: 針對腳本，取得或設定工作的作者。
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- 作者屬性工作排程器
- Author 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，作者屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024546"
---
# <a name="registrationinfoauthor-property"></a>RegistrationInfo. 作者屬性

針對腳本，取得或設定工作的作者。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a>屬性值

工作的作者。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**author**](taskschedulerschema-author-registrationinfotype-element.md) 元素來指定工作作者。

設定這個屬性值時，值可以是從資源 .dll 檔案抓取的文字。 特製化的字串會用來參考資源檔中的文字。 字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ dll \] 是包含資源的 .Dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。 例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 






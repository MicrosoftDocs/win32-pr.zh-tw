---
title: RegistrationInfo 物件
description: 提供可用來描述工作之系統管理資訊的腳本物件。
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- 註冊資訊工作排程器、物件
- RegistrationInfo 物件工作排程器
- RegistrationInfo 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024826"
---
# <a name="registrationinfo-object"></a>RegistrationInfo 物件

提供可用來描述工作之系統管理資訊的腳本物件。 這項資訊包含詳細資料，例如工作的描述、工作的作者、註冊工作的日期，以及工作的安全描述項。

## <a name="members"></a>成員

**RegistrationInfo** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**RegistrationInfo** 物件具有這些屬性。



| 屬性                                                                     | 存取類型           | Description                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**作者**](registrationinfo-author.md)<br/>                         | 讀取/寫入<br/> | 取得或設定工作的作者。<br/>                                                                                            |
| [**日期**](registrationinfo-date.md)<br/>                             | 讀取/寫入<br/> | 取得或設定工作的註冊日期和時間。<br/>                                                                     |
| [**描述**](registrationinfo-description.md)<br/>               | 讀取/寫入<br/> | 取得或設定工作的描述。<br/>                                                                                       |
| [**文件**](registrationinfo-documentation.md)<br/>           | 讀取/寫入<br/> | 取得或設定工作的任何其他檔。<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | 取得或設定工作的安全描述項。<br/>                                                                               |
| [**來源**](registrationinfo-source.md)<br/>                         | 讀取/寫入<br/> | 取得或設定工作源自的位置。 例如，工作可能源自元件、服務、應用程式或使用者。<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | 讀取/寫入<br/> | 取得或設定工作的 URI。<br/>                                                                                               |
| [**版本**](registrationinfo-version.md)<br/>                       | 讀取/寫入<br/> | 取得或設定工作的版本號碼。<br/>                                                                                    |
| [**XmlText**](registrationinfo-xmltext.md)<br/>                       | 讀取/寫入<br/> | 取得或設定工作的 XML 格式版本的註冊資訊。<br/>                                             |



 

## <a name="remarks"></a>備註

註冊資訊可以用來透過工作排程器 UI 來識別工作，或是在列舉已註冊的工作時作為搜尋準則。

讀取或寫入工作的 XML 時，會在工作排程器架構的 [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) 元素中指定工作的註冊資訊。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






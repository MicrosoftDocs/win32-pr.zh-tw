---
title: Win32_RDSHCollection 類別
description: 管理遠端桌面工作階段主機的集合。
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Win32_RDSHCollection 類別遠端桌面服務
- Win32_RDSHCollection 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465549"
---
# <a name="win32_rdshcollection-class"></a>Win32 \_ RDSHCollection 類別

管理遠端桌面工作階段主機的集合。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a>成員

**Win32 \_ RDSHCollection** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ RDSHCollection** 類別具有這些方法。



| 方法                                                                      | 描述                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshcollection.md)           | 抓取 **Win32 \_ RDSHCollection** 物件的整數屬性值。<br/>                                                                                                                  |
| [**GetStringProperty**](getstringproperty-win32-rdshcollection.md)         | 抓取 **Win32 \_ RDSHCollection** 物件的字串屬性值。<br/>                                                                                                                    |
| [**KeyValueCompareAndSet**](win32-rdshcollection-keyvaluecompareandset.md) | 比較集合中指定的索引鍵與比較元;如果相符，索引鍵會設定為新的值。 如果索引鍵不存在，方法會將索引鍵插入集合中。<br/> |
| [**KeyValueDelete**](win32-rdshcollection-keyvaluedelete.md)               | 從集合中刪除指定的索引鍵 (以及相關聯的值) 。<br/>                                                                                                                       |
| [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)                     | 抓取與集合中指定之索引鍵相關聯的值。<br/>                                                                                                                    |
| [**SetInt32Property**](setint32property-win32-rdshcollection.md)           | 更新 **Win32 \_ RDSHCollection** 物件的整數屬性值。<br/>                                                                                                                    |
| [**SetStringProperty**](setstringproperty-win32-rdshcollection.md)         | 更新 **Win32 \_ RDSHCollection** 物件的字串屬性值。<br/>                                                                                                                      |



 

### <a name="properties"></a>屬性

**Win32 \_ RDSHCollection** 類別具有這些屬性。

<dl> <dt>

**別名**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得和設定集合的別名。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得和設定集合的描述。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定集合的名稱。

</dd> <dt>

**型別**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**Windows server 2012 R2 和 Windows server 2012：** 此屬性在 Windows Server 2016 之前無法使用。

集合的類型。

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**一般** (0) 


</dt> <dd></dd> <dt>



 (2)


</dt> <dd>

保留

</dd> <dt>



 (3)


</dt> <dd>

保留

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4) 


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5) 


</dt> <dd></dd> </dl>

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

 


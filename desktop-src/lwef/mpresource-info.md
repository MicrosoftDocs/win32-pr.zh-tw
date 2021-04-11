---
title: 'MPRESOURCE_INFO 結構 (MpClient .h) '
description: 資源資訊結構。
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO 結構舊版 Windows 環境功能
- PMPRESOURCE_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934644"
---
# <a name="mpresource_info-structure"></a>MPRESOURCE \_ 資訊結構

資源資訊結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**方案**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

資源配置識別碼，例如 "file" 或 "dir"。

</dd> <dt>

**路徑**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

資源的絕對路徑（根據 **配置**）。

</dd> <dt>

**類別**
</dt> <dd>

Type： **MPRESOURCE \_ 類別**

</dd> <dd>

當資源被識別為威脅的一部分時，就會設定此欄位。 它會指定資源類別，主要是實體與潛在的。 它可以是下列可能值的組合：



| 值                                                                                                                                                                                                                                                                        | 意義                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_資源 \_ 類別 \_ 不明**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_資源 \_ 類別 \_ 具體**</dt> <dt>0x0001</dt> </dl>           | 互斥于 **MP \_ 資源類別 \_ 的 \_ 潛在**。<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_資源 \_ 類別的 \_ 潛在**</dt> <dt>0x0002</dt> </dl>                 | 互斥于 **MP \_ 資源類別 \_ 的 \_ 實體**。<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_資源 \_ 類別 \_ 範例 \_**</dt>檔案 <dt>0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_資源 \_ 類別 \_ 共用**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 






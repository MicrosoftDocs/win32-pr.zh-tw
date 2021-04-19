---
title: OPAQUECOMMAND 結構
description: OPAQUECOMMAND 結構包含命令的資料，這些命令是透過 Windows Media 裝置管理員傳遞至裝置，但不適合 Windows Media 裝置管理員。
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- OPAQUECOMMAND 結構 windows Media 裝置管理員
- 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998832"
---
# <a name="opaquecommand-structure"></a>OPAQUECOMMAND 結構

**OPAQUECOMMAND** 結構包含命令的資料，這些命令是透過 windows media 裝置管理員傳遞至裝置，但不適合 Windows media 裝置管理員。

## <a name="syntax"></a>語法


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**guidCommand**
</dt> <dd>

代表所要求命令的 **GUID** 。

</dd> <dt>

**dwDataLen**
</dt> <dd>

*.Pdata* 點之資料的長度（以位元組為單位）。

</dd> <dt>

**.Pdata**
</dt> <dd>

執行命令所需的資料，以及（或）命令所傳回的資料。

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

此訊息驗證程式代碼 (MAC) 應該包含 **guidCommand** 成員、 *pdwDataLen* 所指向的資料，以及 *.pdata* 點的資料（如果有的話）。 如果 *.pdata* 為 **Null**，則不得包含在 MAC 中。 WMDM \_ MAC \_ 長度定義為20。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMDSPDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**IMDSPStorage::SendOpaqueCommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**IWMDMDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 






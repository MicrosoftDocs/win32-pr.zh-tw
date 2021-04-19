---
description: 在元件的資訊清單中，抓取與指定 GUID 相關聯的類別名稱和其他資訊。
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983998"
---
# <a name="sxslookupclrguid-function"></a>SxsLookupClrGuid 函式

在元件的資訊清單中，抓取與指定 GUID 相關聯的類別名稱和其他資訊。 只有在 .NET Framework 中執行低層級的 managed 非受控互通性時，才會使用此函數。 如需受管理的非受控互通性的詳細資訊，請參閱 .NET Framework SDK 以及 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)中的「與非受控碼互通」。

## <a name="syntax"></a>語法


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

零或多個下列旗標的組合。



| 值                                                                                                                                                                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SXS \_查閱 \_ CLR \_ GUID \_ 使用 \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | 如果設定此旗標，則 *hActCtx* 參數必須包含 [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) 函數所傳回的啟用內容控制碼。 如果未設定此旗標，則會忽略 *hActCtx* 參數，而 **SxsLookupClrGuid** 會搜尋目前作用中的啟用內容 (使用 [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) 函式來讓啟用內容變成作用中) 。<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SXS \_查閱 \_ CLR \_ GUID \_ 尋找 \_ 代理**</dt> <dt>0x00010000</dt> </dl>  | 如果設定此旗標， **SxsLookupClrGuid** 會搜尋是否有代理。<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SXS \_查閱 \_ clr \_ GUID \_ 尋找 \_ clr \_ 類別**</dt> <dt>0x00020000</dt> </dl> | 如果設定此旗標， **SxsLookupClrGuid** 會搜尋類別。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SXS \_查閱 \_ CLR \_ GUID \_ 尋找 \_ 任何**</dt> <dt>0x00030000</dt> </dl>                    | 這是 **SXS \_ lookup \_ clr \_ Guid \_ find \_ 代理** 和 **SXS \_ lookup \_ clr \_ guid \_ find \_ Clr \_ 類別** 旗標的組合; 如果兩者都已設定， **SxsLookupClrGuid** 就會先搜尋代理，並在找不到它時搜尋某個類別。<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[在\]
</dt> <dd>

指標，指向要在其上搜尋交互操作資訊之啟用內容的 GUID。 此參數不可以是 **Null**。

</dd> <dt>

*hActCtx* \[在中，選擇性\]
</dt> <dd>

如果在 *dwFlags* 參數中設定 **SXS \_ LOOKUP \_ CLR \_ GUID \_ USE \_ ACTCTX** 旗標，則 *hActCtx* 必須包含 [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)函式所傳回的啟用內容控制碼。 否則會忽略 *hActCtx* 。

</dd> <dt>

*pvOutputBuffer* \[in、out、optional\]
</dt> <dd>

要在其中複製傳回信息的緩衝區指標。 只有當 *cbOutputBuffer* 參數為零值時，此參數才可以是 Null 值。 如果有任何) 包含 **SXS \_ GUID \_ 資訊 \_ CLR** 結構，後面接著所需的任何其他字串資料，則會將資料放在這個緩衝區的結束 (。 如需詳細資訊，請參閱下面的「備註」一節。

</dd> <dt>

*cbOutputBuffer* \[在\]
</dt> <dd>

*PvOutputBuffer* 參數所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*pcbOutputBuffer* \[擴展\]
</dt> <dd>

變數的指標，此變數會在結束時放置傳回信息的大小（以位元組為單位）。 如果 *cbOutputBuffer* 參數為零，或如果輸出緩衝區的大小小於傳回信息的大小，則 **SxsLookupClrGuid** 會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 **\_ \_ 緩衝區不足** 的錯誤。 在這種情況下，請使用 *pcbOutputBuffer* 所指向之變數中的值來配置夠大的緩衝區，然後再次呼叫 **SxsLookupClrGuid** 來取出所需的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。 如需詳細的錯誤資訊，請呼叫 [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

Managed 元件可能會將本身宣告為支援 managed 「interop 元件」，以便讓未受管理的 Win32 元件取用者參考宣告元件。 元件取用者可以在 GUID 上呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以與受控元件互動。 交互操作層會將物件建立要求路由至 .NET Framework、建立 managed 物件的實例，並傳回介面指標。

**SxsLookupClrGuid** 可讓架構在元件的資訊清單中，取得與指定 GUID 相關聯的資訊，例如其 .net 類別名稱、所需的 .NET Framework 版本，以及它所在的主機元件。 Managed 元件會發行包含一些語句的 interop 元件，該元件會將 Guid 與元件和類型名稱建立關聯，而 .NET 執行時間會在呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 時，將 managed 物件實例的結構代理程式代理程式。

以下是宣告 CLR GUID 的範例元件資訊清單，以及 **SxsLookupClrGuid** 可以查詢的 clr 代理：

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

互通性提供者會使用 GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" 的指標來呼叫 **SxsLookupClrGuid** ，而且會在中傳回類別名稱 "MySampleSurrogate"、所需的執行階段版本 "1.0.3055"，以及主控元件的文字識別 "DotNet"、version = ' 1.0.0.0 '、type = ' interop ' "。

這項傳回信息會包含及/或由如下所宣告的 **SXS \_ GUID \_ 資訊 \_ CLR** 結構參考。

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

此結構的成員包含下列資訊。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>member</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br/></td>
<td>包含 SXS_GUID_INFORMATION_CLR 結構的大小， (這可讓結構在較新的版本) 中成長。<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br/></td>
<td>包含下列兩個旗標值的其中一個： <br/>
<ul>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001) ：表示指定的 GUID 與代理相關聯 &quot; 。&quot;</li>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002) ：表示指定的 GUID 與類別相關聯 &quot; 。&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br/></td>
<td>指向以零結尾的寬字元字串，識別此類別的主機資訊清單中指定的執行階段版本。<br/></td>
</tr>
<tr class="even">
<td><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br/></td>
<td>指向以零結尾的寬字元字串，其中包含與指定 GUID 相關聯的 .NET 類別名稱。<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br/></td>
<td>指向以零結尾的寬字元字串，其中包含裝載這個類別之元件的文字識別。 如需文字身分識別的詳細資訊，請參閱在 &quot; &quot; &quot; 執行時間 &quot; &quot; 使用 .NET Framework SDK 中的 .NET Framework，在 [在執行時間探索類型資訊] 下指定完整的類型名稱 &quot; 。<br/></td>
</tr>
</tbody>
</table>



 

未受管理的應用程式可以使用以這種方式傳回的資訊來載入正確版本的 .NET Framework、載入 **pcwszAssemblyIdentity** 元素所識別的元件，然後建立 **pcwszTypeName** 專案所命名的類別實例。

## <a name="examples"></a>範例

使用動態連結，如下所示呼叫 **SxsLookupClrGuid** 函數：


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll;</dt><dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[隔離應用程式和並存組件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
